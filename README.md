# Программирование, 2 семестр. Индивидуальное домашнее задание 7. #

## Компиляция и запуск ##

Варианты:

1. Запустить скрипт `./make.sh` для быстрой компиляции и запуска.
2. Прописать вручную `gcc src/main.c -o bin/router; ./bin/router`.


## Задача ##

Массив записей с именем TRAIN, содержит сведения о расписании поездов:

    `{Название пункта назначения; Номер поезда; Время отправления}`.

Написать программу, обеспечивающую ввод с клавиатуры данных в массив
`TRAIN` и вывод на экран информации о поездах, отправляющихся после
введённого с клавиатуры времени. Если таких поездов нет, выдать на
дисплей соответствующее сообщение.


## Анализ задачи ## 

### Структуры данных ###

Все маршруты буду хранить в таблице `route_table`.

Записи в массиве буду хранить в виде структуры `route`:
    
    `{id маршрута; id пункта назначения; Время отправления}`.


Пункты назначения буду хранить в таблице `station_table`.

Записи в массиве буду хранить в виде структуры `station`

    `{id пункта назначения; Название пункта назначения}`.


Время отправления буду хранить в виде структуры `date`:

    `{день; месяц; год; час; минута}`.


### Обращения пользователя ###

Пользователю будет предлагаться ввод с клавиатуры:

    - Целого числа, для ввода id;
    - Последовательности целых чисел для ввода времени;
    - Строки символов, для ввода названия пункта;
    - Символа, для выбора пункта меню для вызова функций ввода или
вывода.
