# My data science project
From the [Skillfactory Data Science Course](https://skillfactory.ru/data-scientist)

## Знакомство с данными. Python для анализа данных.  PYTHON-8. Инструменты для Data Science Финальное задание

### Цель
 Нужно написать программу, которая угадывает число за минимальное число попыток.

 В файле [baseline.ipynb](https://github.com/lunarrray/python_8_final_work/blob/dev/baseline.ipynb) представлены функции написанные авторами курса: 

 random_predict(),  game_core_v2() - угадывают заданное число и возвращают число попыток

score_game() - считает среднее количество попыток угадывание функции

### Задание
Напишите функцию, которая принимает на вход загаданное число и возвращает число попыток угадывания. Для успешного решения задания программа должна угадывать число меньше чем за 20 попыток

### Решение
Функция game_core_v3() написана исполнителем. В отличии от функций авторов курса, тут используется бинарный поиск. 

 Есть два способа использовать бинанрный поиск: с помощью цикла или рекрсивной функции
    В этом случае использована рекурсивная функция find_num
    Смысл бинарного поиска в этой функции в том, чтобы передавать в функцию начало и конец чисел в рамках которых мы ищем число,
    в теле функции будет найдена середина этого промежутка чисел и будет сравниваться с искомым числом, если середина равна искомому возвращаем число,
    если нет сравниваем середину с искомым числом, если середина меньше возвращаем рекурсивную функцию передав как в параметры: начало - середина, конец - конец. 
    Если середина больше искомого числа, возвращаем рекурсивную функцию передав ей как начало - начало, конец - середина. С каждым вызовом функции увеличичвается count(количество попыток угадать)
