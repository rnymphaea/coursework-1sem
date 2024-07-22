Вывод программы должен быть произведен в стандартный поток вывода: stdout.
Ввод данных в программе в стандартный поток ввода: stdin.
В случае использования Makefile название исполняемого файла должно быть: cw.

Важно: первой строкой при запуске программы нужно выводить информацию о варианте курсовой работе и об авторе программы в строго определенном формате:
Course work for option <V>, created by <Name> <Surname>.
Где V – вариант курсовой и Имя и Фамилия, как указано в репозитории группы. Данное предложение должно быть строго первым предложением в выводе программы и является отдельной строкой (заканчивается знаком ‘\n’).

Ввод данных:
После вывода информацию о варианте курсовой работе программа ожидает ввода пользователем числа – номера команды:
0 – вывод текста после первичной обязательной обработки (если предусмотрена заданием данного уровня сложности)
1 – вызов функции под номером 1 из списка задания
2 – вызов функции под номером 2 из списка задания
3 – вызов функции под номером 3 из списка задания
4 – вызов функции под номером 4 из списка задания
5 – вывод справки о функциях, которые реализует программа.
Программа не должна выводить никаких строк, пока пользователь не введет число.

В случае вызова справки (опция 5) текст на вход подаваться не должен, во всех остальных случаях после выбора опции должен быть считан текст.
Признаком конца текста считается два подряд идущих символа переноса строки ‘\n’. После каждой из функций нужно вывести результат работы программы и завершить программу. 
В случае ошибки и невозможности выполнить функцию по какой-либо причине, нужно вывести строку:
	Error: <причина ошибки>

Задание
Каждое предложение должно выводиться в отдельной строке, пустых строк быть не должно. Текст представляет собой предложения, разделенные точкой. Предложения - набор слов, разделенные пробелом или запятой, слова - набор латинских или кириллических букв, цифр и других символов кроме точки, пробела или запятой. Длина текста и каждого предложения заранее не известна.
Для хранения предложения и для хранения текста требуется реализовать структуры Sentence и Text.
Программа должна сохранить (считать) текст в виде динамического массива предложений и оперировать далее только с ним. Функции обработки также должны принимать на вход либо текст (Text), либо предложение (Sentence).
Программа должна найти и удалить все повторно встречающиеся предложения (сравнивать их следует посимвольно, но без учета регистра).
Программа должна выполнить одно из введенных пользователем действий и завершить работу:

### 1) Для каждого предложения вывести строку образец, удовлетворяющую каждому слову в предложении. Строка условия содержит: символы, ? - 1 или больше любых символов, в начале и конце образца могут быть символы * - обозначающие 0 или больше символов. Например, для слов “Аристотель” и “Артишок”, строка образец будет иметь вид “Ар???о?*”. 
### 2) Удалить все предложения, в которых нет заглавных букв в начале слова.
### 3) Отсортировать слова в предложении по количеству гласных букв в слове.
### 4) Для каждого предложения вывести количество одинаковых слов в строке в формате “Количество одинаковых слов: <число>”, где <число> – кол-во одинаковых слов. Пример: “курсовая сдана, курсовая сдана сдана.” -> “Количество одинаковых слов: 5” (потому что 2 раза “курсовая” и 3 раза “сдана”). Слова сравнивать без учёта регистра
Все сортировки и операции со строками должны осуществляться с использованием функций стандартной библиотеки. Использование собственных функций, при наличии аналога среди функций стандартной библиотеки, запрещается.
Каждую подзадачу следует вынести в отдельную функцию, функции сгруппировать в несколько файлов (например, функции обработки текста в один, функции ввода/вывода в другой). Также, должен быть написан Makefile.
