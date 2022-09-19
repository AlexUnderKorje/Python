9-й вариант [группы ИRБО-19-20](http://kispython.ru/group/28).

#### Задача 1

Реализовать функцию.

[Условие задачи](http://kispython.ru/docs/0/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
def main(z, x):
    sk1 = (x**3 + z**2 + 1)**4
    sk2 = 88 * ((z/89)**3)**5
    result = x**3 + z**6 - (sk1 - sk2)
    return result
```

#### Задача 2

Реализовать кусочную функцию.

[Условие задачи](http://kispython.ru/docs/1/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
import math


def main(y):
    if y < 4:
        return function1(y)
    if 4 <= y < 59:
        return function2(y)
    if y >= 59:
        return function3(y)


def function1(y):
    return 35 * math.pow(y, 15) - math.pow(math.tan(y), 2)


def function2(y):
    return (1 + 42 * y + y ** 2) ** 3 + 72 * (y ** 2 - 87 * y ** 3 - y) ** 2


def function3(y):
    return (y ** 4) / 97 + 42 * (abs(y ** 2 + 63)) ** 3 + (y - 1 - 85 * y ** 3) ** 5
```

#### Задача 3

Реализовать итерационную функцию.

[Условие задачи](http://kispython.ru/docs/2/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

<img src="https://user-images.githubusercontent.com/6759207/169617721-bd496f38-2f08-47e3-8ab4-3a4d193272b6.png" width="500" />

```python
def main(a, m, p, b):
    sum1 = 0
    sum2 = 0
    mul1 = 1
    for k in range(1, m + 1):
        for i in range(1, a + 1):
            sum1 += (90 * i - (p ** 2)) ** 5 + 42 + (abs(k) ** 3)
        mul1 *= sum1
        sum1 = 0
    for i in range(1, b):
        y = i ** 3 + 17
        sum2 += y
    return mul1 - sum2
```

#### Задача 4

Реализовать функцию по рекуррентной формуле.

[Условие задачи](http://kispython.ru/docs/3/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
import math


def main(n):
    if n == 0:
        return 0.36
    elif n == 1:
        return -0.91
    elif n >= 2:
        return main(n - 2) + math.sin(main(n - 1)) ** 3
```

#### Задача 5

Реализовать функцию, оперирующую векторами длины n.

[Условие задачи](http://kispython.ru/docs/4/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
import math


def main(z, x):
    result = 0
    n = len(z) - 1
    for i in range(1, n):
        # print(i)
        # print((n + 1) - math.floor(i / 2))
        result += math.sqrt((0.09 + x[i] + z[(n + 1) - math.ceil(i / 2)] ** 2)**4)

    return result * 7

```

#### Задача 6

Реализовать функцию для вычисления дерева решений.

[Условие задачи](http://kispython.ru/docs/5/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
def zero(items, left, midle, right):
    if items[0] == 1987:
        return left
    if items[0] == 1989:
        return midle
    if items[0] == 2015:
        return right


def three(items, left, midle, right):
    if items[3] == 'URWEB':
        return left
    if items[3] == 'HAXE':
        return midle
    if items[3] == 'HACK':
        return right


def one(items, left, right):
    if items[1] == 'AGDA':
        return left
    if items[1] == 'BISON':
        return right



def twoo(items, left, right):
    if items[2] == 2015:
        return left
    if items[2] == 1984:
        return right

def main(items):
    return one(
        items,
        three(items, zero(items, 0, 1, 2), 3, 4),
        three(items, zero(items, 5, 6, 7), twoo(items, 8, 9), 10)
    )
```

#### Задача 7

Реализовать функцию для преобразования битовых полей.

[Условие задачи](http://kispython.ru/docs/6/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
def main(input):
    a = (input & 0b00000000000000001111111111111111) << 16
    b = (input & 0b00000000000000110000000000000000) >> 16
    c = (input & 0b00001111111111000000000000000000) >> 16
    d = (input & 0b11110000000000000000000000000000) >> 16

    return a | b | c | d
```

#### Задача 8

Реализовать функцию для разбора строки, содержащей данные в текстовом формате.

> Для отладки [регулярных выражений](https://docs.python.org/3/library/re.html) можно воспользоваться сервисом [regexr.com](http://regexr.com) или [regex101.com](https://regex101.com/)

[Условие задачи](http://kispython.ru/docs/7/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
import re

string_1 = r"do .do auto #4108 -> veusce; .end .do auto #438 -> temara_645; .end.do auto#2811" \
           r" -> arusza;.end .do auto#3041 -> geis_155; .end od"
x = r"#[-+]?\d+"
y = r">.{1,15};"
my_dict = {}
numb = re.findall(x, string_1)
str2 = re.findall(y, string_1)
for i in range(len(str2)):
    str2[i] = str2[i].replace('> ', '')
    str2[i] = str2[i].replace(' ', '')
    str2[i] = str2[i].replace(';', '')
for i in range(len(numb)):
    numb[i] = numb[i].replace('#', '')
    numb[i] = int(numb[i])
    my_dict[str2[i]] = numb[i]

```

#### Задача 9

Реализовать конечный автомат Мили в виде класса.

[Условие задачи](http://kispython.ru/docs/8/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
from enum import Enum


class State(Enum):
    A = 0
    B = 1
    C = 2
    D = 3
    E = 4
    F = 5
    G = 6


class StateMachine:
    state = State.A

    def warp(self):
        return self.update({
            State.A: [State.B, 0],
            State.B: [State.C, 2],
            State.E: [State.B, 7],
        })

    def view(self):
        return self.update({
            State.A: [State.D, 1],
            State.E: [State.F, 5],
            State.F: [State.G, 8],
        })

    def carve(self):
        return self.update({
            State.C: [State.D, 3],
            State.D: [State.E, 4],
            State.E: [State.E, 6],
            State.F: [State.C, 9],
        })

    def update(self, transitions):
        self.state, signal = transitions[self.state]
        return signal


def main():
    return StateMachine()
```

#### Задача 10

Реализовать функцию преобразования табличных данных. 

[Условие задачи](http://kispython.ru/docs/9/%D0%98%D0%9A%D0%91%D0%9E-19-20.html#%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82-9)

```python
import re

table = [[None, '11-10-2003', 'Y', '57%', 'Василий И. Симелян'],
         [None, '24-11-2004', 'N', '32%', 'Тамерлан Б. Зисилин'],
         [None, '05-04-2002', 'Y', '11%', 'Тамерлан А. Мелизяк'],
         [None, '25-04-2002', 'N', '33%', 'Николай А. Мацезян']]


def main(table):
    table = rem_none_two(glob_none(povtorenii(table)))
    for i in range(len(table)):
        table[i][0] = table[i][0][6:] + table[i][0][2:6] + table[i][0][:2]
        if table[i][1] == 'Y':
            table[i][1] = 'Да'
        else:
            table[i][1] = 'Нет'
        if table[i][2] == '100%':
            table[i][2] = '1.0'
        elif table[i][2] == '0%':
            table[i][2] = '0.0'
        else:
            table[i][2] = table[i][2].replace('%', '')
            table[i][2] = '0.' + table[i][2]
            table[i][2] = float(table[i][2])
            table[i][2] = round(table[i][2], 1)
        format_name = r" .[.].{1,}"
        true_name = re.findall(format_name, table[i][3])
        table[i][3] = table[i][3][0:1] + '.' + true_name[0]
    print(perevertish(table))


def glob_none(table):
    for elem in table:
        if elem == [None, None, None, None, None]:
            table.remove(elem)
    return table


def rem_none_two(table):
    for elem in table:
        while elem.count(None) != 0:
            elem.remove(None)
    return table


def povtorenii(table):
    table.reverse()
    for i in table:
        while table.count(i) != 1:
            table.remove(i)
    table.reverse()
    return table


def perevertish(table):
    my_list_data = []
    my_list_danet = []
    my_list_proc = []
    my_list_name = []
    for i in range(len(table)):
        my_list_data.append(table[i][0])
        my_list_danet.append(table[i][1])
        my_list_proc.append(table[i][2])
        my_list_name.append(table[i][3])
    table = [my_list_data, my_list_danet, my_list_proc, my_list_name]
    return table


main(table)
```

