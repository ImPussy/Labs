# Тема 8. Введение в ООП
Отчет по Теме #8 выполнил(а):
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
### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.


```python
class Paper:
    def __init__(self, name):
        self.name = name

p1 = Paper('Газетная')
print(p1.name)
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/picturesLab8/1.jpg)

## Выводы
текст
  
## Самостоятельная работа №2
### Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Paper:
    def __init__(self, name, cost):
        self.name = name
        self.cost = cost

    def info(self):
        print(f"Информация о бумаге:\nНазвание: {self.name}\nСтоимость: {self.cost}")

p1 = Paper('Газетная', 12)
p1.info()

p2 = Paper("Картон", 44)
p2.info()
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/picturesLab8/2.jpg)

## Выводы
текст
  
## Самостоятельная работа №3
### Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Paper:
    def __init__(self, name, cost):
        self.name = name
        self.cost = cost

    def info(self):
        print(f"Информация о бумаге:\nНазвание: {self.name}, Стоимость: {self.cost}")

class Paper2(Paper):
    def __init__(self, name, cost, color):
        super().__init__(name, cost)
        self.color = color

    def full_info(self):
        print(f"Информация о бумаге:\nНазвание: {self.name}, Стоимость: {self.cost}, Цвет: {self.color}")

p1 = Paper('Газетная', 12)
p1.info()
print("")

p2 = Paper2("Картон", 44, "коричневый")
p2.full_info()
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/picturesLab8/3.jpg)

## Выводы
текст
  
## Самостоятельная работа №4
### Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Paper:
    def __init__(self, name, cost):
        self._name = name
        self._cost = cost

    def info(self):
        return f"Информация о бумаге:\nНазвание: {self._name}, Стоимость: {self._cost}"

p1 = Paper('Газетная', 12)
print(p1._name)
print(p1.info())
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/picturesLab8/4.jpg)

## Выводы
текст
  
## Самостоятельная работа №5
### Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Paper:
    def __init__(self, name, cost):
        self.name = name
        self.cost = cost
    def info(self):
        print(f"Информация о бумаге:\nНазвание: {self.name}, Стоимость: {self.cost}")

class Paper2(Paper):
    def __init__(self, name, cost, color):
        super().__init__(name, cost)
        self.color = color
    def info(self):
        print(f"Информация о бумаге:\nНазвание: {self.name}, Стоимость: {self.cost}, Цвет: {self.color}")

class Paper3(Paper):
    def __init__(self, name, cost, size):
        super().__init__(name, cost)
        self.size = size
    def info(self):
        print(f"Информация о бумаге:\nНазвание: {self.name}, Стоимость: {self.cost}, Размер: {self.size}")

p1 = Paper('Газетная', 12)
p1.info()

p2 = Paper2("Картон", 44, "коричневый")
p2.info()

p3 = Paper3("Картон", 44, "1000х500")
p3.info()
```

### Результат.
![Меню](https://github.com/ImPussy/Labs/blob/%D0%A2%D0%B5%D0%BC%D0%B0_8/picturesLab8/5.jpg)

## Выводы
текст

## Общие выводы по теме
текст
