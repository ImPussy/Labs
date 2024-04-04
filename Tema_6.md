# Тема 6. Базовые коллекции: словари, кортежи
Отчет по Теме #6 выполнил(а):
- Кантуганов Тимур Эдуардович
- ИНО ЗБ ПОАС-22-1

| Задание | Сам_раб |
| ------ | ------ |
| Задание 1 | + |
| Задание 2 | + |
| Задание 3 | + |
| Задание 4 | + |
| Задание 5 | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Самостоятельная работа №1
### При создании сайта у вас возникла потребность обрабатывать данные пользователя в странной форме, а потом переводить их в нужные вам форматы.


```python
numbers = input('Введите числа через пробел: ')
l = numbers.split()
t = tuple(numbers.split())
print(l, t, sep='\n')
```
### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_6/picturesLab6/1.jpg)

## Выводы
текст
  
## Самостоятельная работа №2
### Николай знает, что кортежи являются неизменяемыми, но он очень упрямый и всегда хочет доказать, что он прав.

```python
numbers = ['(1, 2, 3), 1)', '(1, 2, 3, 1, 2, 3, 4, 5, 2, 3, 4, 2, 4, 2), 3)', '(2, 4, 6, 6, 4, 2), 9)']

def rem(t, el):
    l = list(t)
    if el in l:
        l.remove(el)
        return tuple(l)
    else:
        return t

for tple in numbers:
    t = tuple(map(int, tple[:-4].strip('()').split(',')))
    element = int(t[-2:-1][0])
    new_tuple = rem(t, element)
    print(new_tuple)
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_6/picturesLab6/2.jpg)

## Выводы
текст
  
## Самостоятельная работа №3
### Ребята поспорили кто из них одним нажатием на numpad наберет больше повторяющихся цифр, но не понимают, как узнать победителя.

```python
nums = input('Нажмите ладонью на numpad один раз\n')

def count_numbers(string):
    num_freq = {}

    for i in string:
        i = int(i)
        num_freq[i] = num_freq.get(i, 0) + 1

    sorted_num_freq = sorted(num_freq.items(), key=lambda item: item[1])
    top_three = dict(sorted(sorted_num_freq[-3:]))
    return top_three

print(count_numbers(nums))
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_6/picturesLab6/3.jpg)

## Выводы
текст
  
## Самостоятельная работа №4
### Ваш хороший друг владеет офисом со входом по электронным картам, ему нужно чтобы вы написали программу, которая показывала в каком порядке сотрудники входили и выходили из офиса.

```python
tuples = ['(1, 2, 3), 8)', '(1, 8, 3, 4, 8, 8, 9, 2), 8)', '(1, 2, 8, 5, 1, 2, 9), 8)']

def find_element(tple, element):
    if tple.count(element) > 0:
        start_index = tple.index(element)
        end_index = tple.index(element, start_index + 1) if tple.count(element) > 1 else ()
        return tple[start_index:end_index + 1] if end_index != () else tple[start_index:]
    else:
        return ()

for tpl in tuples:
    tple = tuple(map(int, tpl[1:-4].strip('()').split(',')))
    element = int(tpl[-2])
    new_tuple = find_element(tple, element)
    print(new_tuple)
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_6/picturesLab6/4.jpg)

## Выводы
текст
  
## Самостоятельная работа №5
### В магазине продается бумага разного типа. На складе имеется информация о количестве каждого типа и их средней цене. Необходимо посчитать общую стоимость всей бумаги на складе.

```python
paper_info = [('Газетная', 100), ('Дизайнерская', 50), ('Картон', 75)] # Тип бумаги и кол-во на складе
paper_prices = {'Газетная': 12, 'Дизайнерская': 79, 'Картон': 20} # Тип бумаги и средняя цена

total_cost = 0

for paper_type, counts in paper_info:
    paper_price = paper_prices[paper_type]
    total_cost += counts * paper_price

print(f"Общая стоимость всей бумаги на складе: {total_cost} рублей.")
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_6/picturesLab6/5.jpg)

## Выводы
текст

## Общие выводы по теме
текст
