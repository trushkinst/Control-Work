Ход решения задачи

1.Схема 
![image](https://user-images.githubusercontent.com/112189215/195981018-de307039-f1ae-4673-9218-8b52c8a73cbd.png)

Получившаяся схема

Описывая алгоритм можно сказать следующее

Для начала определялся исходный массив. Я решил задать его из разных букв и цифр в различном регистре. Сделано это для упрощения проверки решения. Проблем задать перебором введения значений каждого предлагаемого массива и определения длины не покажет мое "невероятное знание языка", а лишь усложнит работу проверяющего.

Задав стартовый массив была опеределена функция поиска трехсимвольных строк SearchForThrdCharString

(прим. Название считаю достаточным для понимания)

Понимая, что каждый элемент массива это строка, а в языке C# она, эта строка, будет представленна как массив (Вот такой массив массивов 😏), Я использовал условие на проверку количества элементов(символов) в массиве-строке.

Отлавливая все массивы-строки с количеством элеметов 3 или менее конструкцией if я присваивал значения в новом массиве out_mas по адресу j. -Отдельная интересная история с выъодным массивом. Я не мог обойтись вторым счетчиком конструкции for. Нужно было, что бы элемент наращивался только при нахождении подходящей строки. И не было понятно, какого объема должен был быть выходной массив.

Здесь на помощь пришел метод Array.Resize и вынесения j за цикл. Каждую итерацию, при нахождении элемента, я переопределяю длину выходного массива на величину 1 + j. И правда, таким образом вводимый массив может быть любым. А выходной массив будет без пустых клеток.
