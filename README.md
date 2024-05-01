# Кубик Рубика
Программа для визуализации и сборки кубика Рубика.

## Описание 
Программа предоставляет двумерную визуализацию кубика Рубика 3x3 с возможностью управления поворотами граней с клавиатуры. 

## Запуск программы
Создайте виртуальную среду
```
$ virtualenv venv
```
Активируйте виртуальную среду
```
$ source venv/bin/activate
```
Установите зависимости
```
$ pip install -r requirements.txt
```
Запустите GUI
```
$ python3 -m src.main
```

## Структура проекта

### ``src/cube``

Этот каталог включает основную логику, связанную с моделированием кубика Рубика и его алгоритмами решения.

- ``gui.py``: Класс Gui служит мостом между классом куба и библиотекой Pygame.

- ``cube.py``: Класс Cube, который содержит основную логику работы с кубиком Рубика.

- ``history_cube.py``: Расширение класса Cube, добавляющее функционал для записи всех сделанных ходов.

- ``solver.py``: Функции для вычисления решений для заданного экземпляра кубика.

- ``move.py``: Простой класс для хранения информации о ходах.

- ``pieces.py``: Классы данных для элементов Edge и Corner, инкапсулирующие детали этих частей кубика.

- ``colour.py``: Определение типа для цветов, используемое для представления RGB цветов.

### ``src/scramble``

Каталог для алгоритмов генерации и анализа начальных перестановок кубика.


- ``generator.py``: Функция для создания начальной перестановки путем случайного выбора ходов.

- ``parser.py``: Функции для анализа и преобразования ходов из строк в тип Move.

### ``src/stats``

Содержит функции для статистического анализа работы алгоритмов решения.

- ``statistics.py``: Класс для генерации статистических данных, включая запись количества ходов в электронную таблицу.

### ``tests``

Тесты для проверки функционала программы, запускаемые с помощью команды python3 -m pytest.

- ``test_cube.py``: Тесты для проверки целостности данных куба и функций решателя.
