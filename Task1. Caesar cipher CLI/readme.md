# Caesar cipher CLI tool (Task 1 on RSS 2020 NodeJS)

Утилита командной строки для кодирования/декодирования простейшим шифром Цезаря со смещением букв алфавита. [Ссылка на задание](https://github.com/rolling-scopes-school/nodejs-course-template/blob/master/TASKS.md#task-1-caesar-cipher-cli-tool)

### Утилита принимает на вход 4 аргумента, в коротком или длинном стиле:
-s, --shift: смещение шифра Цезаря  
-i, --input: путь к входному файлу  
-o, --output: путь к выходному файлу  
-a, --action: действие - кодировать (encode) или декодировать (decode)  

### Детали:
1. Обязательными аргументами являются Действие (action) и Смещение (shift), если один из них пропущен, то будет выдана ошибка и программа завершится со статусом, не равным нулю.
2. Если не задан путь к входному файлу (input), то используется стандартный ввод stdin.
3. Если не задан путь к выходному файлу (output), то используется стандартный вывод stdout.
4. Кодируются и декодируются только буквы латинского алфавита (заглавные и строчные), все остальные символы остаются без изменений.

### Варианты вызова утилиты:
$ node caesar_cli -a encode -s 7 -i "./input.txt" -o "./output.txt"  
$ node caesar_cli --action encode --shift 7 --input plain.txt --output encoded.txt  
$ node caesar_cli --action decode --shift 7 --input decoded.txt --output plain.txt  
