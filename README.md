# Decimal

### Реализация собственной библиотеки s21_decimal.h, двоичное представление Decimal имеет вид ((от -2^96 до 2^96) / 10^(от 0 до 28)). 

__Арифметические операторы__
  1. __int s21_add(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)__ - сложение.
  2. __int s21_sub(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)__ - вычитание.
  3. __int s21_mul(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)__ - уножение.
  4. __int s21_div(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)__ - деление.
  5. __int s21_mod(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)__ - остаток от деления.
  ```
  __Функции возвращают код ошибки:__
  * 0 - OK
  * 1 - число слишком велико или равно бесконечности
  * 2 - число слишком мало или равно отрицательной бесконечности
  * 3 - деление на 0
```
__Операторы сравнения:__
  1. __int s21_is_less(s21_decimal, s21_decimal)__ -             меньше.
  2. __int s21_is_less_or_equal(s21_decimal, s21_decimal)__ -    меньше или равно.
  3. __int s21_is_greater(s21_decimal, s21_decimal)__ -          больше.
  4. __int s21_is_greater_or_equal(s21_decimal, s21_decimal)__ - больше или равно.
  5. __int s21_is_equal(s21_decimal, s21_decimal)__ -            равно.
  6. __int s21_is_not_equal(s21_decimal, s21_decimal)__ -        не равно.
  ```
  __Возвращаемое значение:__
  * 0 - FALSE
  * 1 - TRUE
```
__Преобразователи:__
  1. __int s21_from_int_to_decimal(int src, s21_decimal *dst)__ -     из int в decimal.
  2. __int s21_from_float_to_decimal(float src, s21_decimal *dst)__ - из float в decimal.
  3. __int s21_from_decimal_to_int(s21_decimal src, int *dst)__ -     из decimal в int.
  4. __int s21_from_decimal_to_float(s21_decimal src, float *dst)__ - из decimal в float.
  ```
  Возвращаемое значение - код ошибки:
  * 0 - OK
  * 1 - ошибка конвертации
  ```
__Другие функции:__
  1. __int s21_floor(s21_decimal value, s21_decimal *result)__ -    округляет указанное Decimal число до ближайшего целого числа в сторону отрицательной бесконечности.
  2. __int s21_round(s21_decimal value, s21_decimal *result)__ -    округляет Decimal до ближайшего целого числа.
  3. __int s21_truncate(s21_decimal value, s21_decimal *result)__ - возвращает целые цифры указанного Decimal числа; любые дробные цифры отбрасываются, включая конечные нули.
  4. __int s21_negate(s21_decimal value, s21_decimal *result)__ -   возвращает результат умножения указанного Decimal на -1.
  ```Возвращаемое значение - код ошибки:
  * 0 - OK
  * 1 - ошибка вычисления
  ```
