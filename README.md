# RegExr-CheatSheet
CheatSheet of RegExr js

* . - любой символ
* [aAbB] - любой из них.

> [a-d] - диапозон
> [0-9].[0-9] - дроби Devsd
> $ - конец строки
> ^ - Начало строки
> \ - Экранирование.
> \n - перенос строки.
> [^a] - отрицание не а
> \d - любая цыфра \d\d - ц цыфры и т.д
> \D - все что угодно кроме цыфр
> \s - пробелы пример: Know - /ow\s/g найдет последние ow и пробел
> \S - Все кроме пробела
> \w - любая буква пример: \w\w - любые 2 буквы
> \b - выделяет границу слова например слово how -  \b\w\w\w\b
> \B - Все кроме пробела не границ
> i без учета регистра
## квантификаторы
> \b\w{3}\b = заменяет длинное написание \b\w\w\w\b
> n{4} -
> r{1,3} ищет r от 1 до 3

> * от нуля и выше ищет совподения например в слове knooooww /kno*/g найдет knoooo
> + от 1 и выше
> ? либо 0 либо 1 - например /\d{4}.?/g найлеи весь номер кредитки 4444 0000 5555 6999
> | и тоже самое тольк внутри массива [\d-] - любая цыфраи -

### Example
let str =
  'asfasdffrfkm;asdmnab vaidiuojmckasdacлтknvmnjavbf knooooww qdkoqof jasdovnsdl'
let num = '4441-4444 6666 8888 8548+888'
let mail = 'mad@gmail.com'

let regExp = /\d{4}|\d{3}|\+/g
let numReg = /4?\d{4}/g
let mailReg = /\w+@\w+\.\w{2}|\w{3}/g

const val = mail.match(mailReg)

console.log(val ? true : false)

### replace 
let phoneNum = '+7 (968) 607 96-65'
const phoneNumClear = phoneNum.replace(/[+\(\s-)]/gi, (count, index, arr) => {
  return '' > удалит все плюсы пробелы, тире, и скобки
})
