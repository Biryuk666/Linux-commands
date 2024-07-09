## Введение
Данный репозиторий является форком `JavaZakariae/Linux-commands`, переведенным на русский язык.

Этот репозиторий не предназначен для объяснения операционной системы Linux, но он может быть очень полезен как напоминание о том, как работает определенная команда Linux. В первой части этого репозитория вы можете найти хорошие примеры практически всего, что связано с командами Linux, во второй части вы найдете все, что связано с программированием в командной строке.

- [Команды Linux](#команды-linux)
  - [Помощь](#помощь)
  - [Полезные и часто используемые команды Linux](#полезные-и-часто-используемые-команды-linux)
  - [Типы файлов Linux](#типы-файлов-linux)
  - [Терминал:](#терминал)
  - [Система навигации по файлам](#система-навигации-по-файлам)
  - [Подкаталоги Linux](#подкаталоги-linux)
  - [Команда `ls` и ее флаги](#команда-ls-и-ее-флаги)
  - [Создание каталога](#создание-каталога)
  - [Команды `rm` and `rmdir`. Удаление каталогов](#команды-rm-and-rmdir-удаление-каталогов)
  - [Копирование, перемещение и переименование файлов и каталогов](#копирование-перемещение-и-переименование-файлов-и-каталогов)
  - [Создание файлов при помощи команд `cat`, `touch`, `gedit` и `vi`](#создание-файлов-при-помощи-команд-cat-touch-gedit-и-vi)
  - [Просмотр содержимого файлов при помощи команд `cat`, `tac`, `rev`, `head` и `tail`](#просмотр-содержимого-файлов-при-помощи-команд-cat-tac-rev-head-и-tail)
  - [View files content using less and more](#view-files-content-using-less-and-more)
  - [Creation of hidden files and directories](#creation-of-hidden-files-and-directories)
  - [Copying moving and renaiming files and directories using cp and mv commands (2)](#copying-moving-and-renaiming-files-and-directories-using-cp-and-mv-commands-2)
  - [Comparing content of files (diff sdiff...)](#comparing-content-of-files-diff-sdiff)
  - [Soft and hard link](#soft-and-hard-link)
  - [Sort commands](#sort-commands)
  - [Uniq commands](#uniq-commands)
  - [Input and Output](#input-and-output)
  - [Redirecting stdInput stdOutput and stdError](#redirecting-stdinput-stdoutput-and-stderror)
  - [Piping](#piping)
  - [Execute multiple command](#execute-multiple-command)
  - [Commands aliasing](#commands-aliasing)
  - [Regular expressions](#regular-expressions)
  - [locate](#locate)
  - [find command](#find-command)
  - [Compression and uncompression of files (episode 33)](#compression-and-uncompression-of-files-episode-33)
      - [Creation of archive files](#creation-of-archive-files)
      - [Apply compression algorithm on archive files (gzip bzip2)](#apply-compression-algorithm-on-archive-files-gzip-bzip2)
  - [grep command](#grep-command)
  - [Regular expressions patterns](#regular-expressions-patterns)
      - [Character Patterns](#character-patterns)
      - [Word Patterns](#word-patterns)
      - [Line Patterns](#line-patterns)
      - [Additional Patterns available only when using the egrep command](#additional-patterns-available-only-when-using-the-egrep-command)
  - [The cut command](#the-cut-command)
  - [The Linux File Permissions Concept](#the-linux-file-permissions-concept)
      - [User categories](#user-categories)
      - [Permission types](#permission-types)
      - [Operations allowed related permissions](#operations-allowed-related-permissions)
      - [Users and groups](#users-and-groups)
      - [Umask](#umask)
  - [Working with editors](#working-with-editors)
  - [Checking Resource Usage](#checking-resource-usage)
  - [Package Management(ubuntu)](#package-managementubuntu)
  - [Managing systemd units](#managing-systemd-units)
  - [Viewing Logs](#viewing-logs)
  - [Managing users](#managing-users)
  - [SSH](#ssh)
  - [Bash history](#bash-history)
  - [Process control commands](#process-control-commands)
    - [Types of processes](#types-of-processes)
    - [background/foreground mode](#backgroundforeground-mode)
    - [ps command:](#ps-command)
    - [top command:](#top-command)
    - [kill command:](#kill-command)
  - [Network linux commands](#network-linux-commands)
  - [man page](#man-page)
  - [curl command](#curl-command)
  - [Stackoverflow questions](#stackoverflow-questions)
- [Shell scripting](#shell-scripting)
  - [What is Shell?](#what-is-shell)
  - [Types of Shell?](#types-of-shell)
  - [Scripts and Shell info](#scripts-and-shell-info)
  - [Variables in Shell programming](#variables-in-shell-programming)
      - [Predifined variables (environement variables)](#predifined-variables-environement-variables)
      - [User defined variables](#user-defined-variables)
        - [variables name](#variables-name)
      - [variable scopes](#variable-scopes)
      - [Variable substitution](#variable-substitution)
      - [Command substitution](#command-substitution)
      - [Command Line arguments](#command-line-arguments)
      - [Read dynamic data from the user](#read-dynamic-data-from-the-user)
      - [Operators](#operators)
      - [How to perform matematical operations](#how-to-perform-matematical-operations)
      - [Control statements](#control-statements)
        - [if statement](#if-statement)
        - [Exit codes / Status codes](#exit-codes--status-codes)
        - [File test options](#file-test-options)
        - [String test options](#string-test-options)
        - [case statement](#case-statement)
        - [while loop](#while-loop)
        - [break and continue](#break-and-continue)
        - [for loop](#for-loop)
      - [Arrays concept](#arrays-concept)
        - [How to create arrays](#how-to-create-arrays)
        - [How to access arrays](#how-to-access-arrays)
        - [Examples](#examples)
      - [Shell Script Functions](#shell-script-functions)
        - [How to define a function](#how-to-define-a-function)
        - [Varibale scopes](#varibale-scopes)
        - [Return statement](#return-statement)
        - [break vs exit vs return](#break-vs-exit-vs-return)
        - [How to call functions present in another script](#how-to-call-functions-present-in-another-script)
  - [Various topics](#various-topics)

# Команды Linux
## Помощь
- `man, help, apropos, whereis, whatis, which`: команды, которые дают справку по указанной команде.
- `man -k text`: ищет команды, содержащие в своем описании заданный текст.
- `mandb`: обновляет справочные страницы до последней версии.
- `updatedb`: обновляет базу данных, чтобы поиск местоположения включал последние добавленные файлы.

## Полезные и часто используемые команды Linux
- Узнать сколько пользователей зарегистрировано в системе: `who`
- Кто текущий пользователь: `whoami`
- Показать календарь: `cal`
- Вывести рабочий каталог(дерикторию): `pwd`
- Вывести список файлов и внутренних каталогов текущего каталога: `ls`
- Ручная помощь: `man whoami`
- Создайте новый каталог: `mkdir имя_каталога`
- Создайте новый пустой файл: `touch имя_файла`
- Удалить каталог: `rmdir имя_каталога`
- Удалить файл: `rm имя_файла`
- Удалить каталог и его содержимое: `rm -r имя_каталога`
- Отобразить список доступных команд: `help`
- Очистить терминал: `clear`, `ctrl+l`
- Выход из сеанса: `exit`
- Отобразить дату: `date`
- Отобразить время: `time`
- Распечатать информацию: `hello`
- Увеличьте размер шрифта: `Ctrl + Shift + '+'`
- Напечатать 5 случайных чисел от 1 до 100: `shuf -i 1-100 -n 5`
- Создать файл использующий команду `shuf`: `touch dir$(shuf -i 1-10 -n 1)/sunny.txt`
- Простой пользователь: `$ prompt`
- Корневой пользователь/администратор: `# prompt`
- Сменить простого на корневого пользователя: `sudo -i`
- Сменить корневого на простого пользователя:  `exit`

## Типы файлов Linux

Чтобы показать тип файла, используйте команду `file имя_файла`. Linux читает файлы на основе их содержимого, а не на основе их расширений. Linux имеет следующие типы фалов:
- Каталог или directory file.
- Обычный файл или normal file (бинарный или текстовый).
- Файл устройства или device file: каждое устройство представлено в виде файла.

## Терминал:
- чтобы открыть терминал, используйте горячие клавиши `ctrl + alt + t`.
- Для закрытия терминала, используйте `ctrl + d`.
- Чтобы показать файл, представляющий текущий терминал, используйте команду `tty`, которая выведет путь к файлу: /dev/pts/0
- Чтобы показать файлы в текущем каталоге, используйте команду `ls -l`, где `-l` означает длинный список (long listing)."

## Система навигации по файлам

Домашний каталог находится по адресу: `/home/имя_пользователя`, где `/home` содержит домашние каталоги всех пользователей, а `/` - это самый верхний корень.
- Отобразить скрытые файлы: `ls -a`, где  `-a`означает все (all).
- Перейи в домашний каталог: `cd` или `cd ~`
- Перейти в предыдущий каталог: `cd -`

## Подкаталоги Linux

- `bin` каталог: он содержит все исполняемые двоичные файлы, относящиеся к нашим командам Linux, `which touch` выведет `/user/bin/touch`
- `sbin` каталог: он содержит все исполняемые двоичные файлы, относящиеся к суперпользователю.
- `etc` каталог: он содержит информацию о конфигурации системы, требуемую операционной системой, например пароли пользователей `/etc/passwd`, информацию о группах `/etc/group` и информацию о хостах `/etc/hosts`(ip адреса и dns имена).
- `tmp` каталог: `tmp` означает временный (temporary). Если какой-либо файл или каталог является временным, он создается в папке `tmp` в текущем сеансе. содержимое каталога будет удалено автоматически после завершения работы.
- `dev` каталог: `dev` означает устройство (device). Все файлы, относящиеся к устройству, будут храниться в этом каталоге. Используя их, мы можем взаимодействовать с устройством.
- `mnt` каталог: `mnt` означает монтирование (mount). В него системные администраторы могут монтировать внешние или дополнительные файловые системы
- `opt` каталог: `opt` означает оциональный (optional). Он содержит все установочные файлы программного обеспечения сторонних производителей.
- `lib` каталог: `lib` означает библиотеки (libraries), которые требуются в приложениях.
- `var` каталог: `var` означает переменные данные (variable data). В этом каталоге будут храниться переменные данные, например файлы журналов.
- `usr` каталог:  `usr` означает системные ресурсы пользователя (user system resources). Он содержит программное обеспечение, связанное со всеми пользователями.
- `home` каталог: у каждого пользователя есть отдельная папка для хранения его конкретных данных, таких как изображения, документы и так далее.
- `root` каталог: домашний каталог супер пользователя.
- `proc` каталог: `proc` означает процесс (process), для каждого процесса присваивается уникальный идентификатор, и внутри папки `proc` будет создан отдельный каталог.
- `boot` каталог: он содержит файлы, необходимые для загрузки системы Linux.

## Команда `ls` и ее флаги

- Вывести список всех файлов и каталогов, находящихся в каталоге `dir1`: `ls dir1`
- Вывести список файлов и внутренних каталогов текущего каталога: `ls`
- Вывести список в обратном алфавитном порядке: `ls -r`
- Вывести список в расширенном формате (более подробно о содержании): `ls -l`
- Вывести список в зависимости от времени создания: `ls -t`
Можно комбинировать все вышеперечисленные опции: `ls -ltr`
- Вывести список включая скрытые файлы: `ls -a`
- Вывести список по типу: `ls -F`
- Вывести список рекурсивно: `ls -R`
- Вывести список с общим размером (1 блок = 1024kb): `ls -s`
- Вывести список из 10 верхних записей: `ls -l /имя_каталога | head`
- Вывести список из 5 верхних записей: `ls -l /имя_каталога | head -5`
- Вывести список из 10 нижних записей: `ls -l /имя_каталога | tail`
- Вывести список страницу за страницей: `ls -l /имя_каталога | more` или `ls -l /имя_каталога | less`, `less` более мощный инструмент (работает в 2-х направлениях: вперед и назад).

## Создание каталога

- Создать каталог в этом же каталоге: `mkdir имя_каталога`
- Создать сразу несколько каталогов в этом же каталоге: `mkdir имя_каталога1 имя_каталога2 имя_каталога3`
- Создать сразу несколько каталогов вглубь в этом же каталоге: `mkdir -p имя_каталога1/имя_каталога2/имя_каталога3`. Здесь `имя_каталога1, имя_каталога2` будут созданы только в том случае, если они еще не существуют.
- Создать сразу несколько каталогов вглубь в этом же каталоге и заполнить некоторые из них другими каталогами: `mkdir -p имя_каталога1/имя_каталога2{имя_каталога3-1,имя_каталога3-2,имя_каталога3-3}/имя_каталога{1..31}`. Здесь каждый `имя_каталога3-X` будет содержать 31 каталог.
- Показать  содержимое каталога в виде древовидной структуры данных:  `tree`

## Команды `rm` and `rmdir`. Удаление каталогов

- Удалить файл: `rm имя_файла`
- Удалить пустой каталоги: `rmdir имя_каталога1 имя_каталога2`
- Удалить каталог вместе с файлами: `rm -r имя_каталога`, или `rm -R имя_каталога`. Для удаления обычных файлов флаг `-r` не нужен.
- Чтобы получить подтверждение перед удалением содержимого:: `rm -r -i имя_каталога`
- Принудительное удаление `-f`: `rm -rf имя_каталога`
- Вывести ход процесса при удалени `v`: `rm -rv имя_каталога`

## Копирование, перемещение и переименование файлов и каталогов

- Копировать содержимое файла из одного файла в другой: `cp имя_файла1 имя_файла2`. Если `имя_файла2` не существует, будет создан новый файл, если нет, то файл будет перезаписан.
- Копировать содержимое в другое место: `cp имя_файла1 home/имя_каталога/имя_файла2`.
- Копировать несколько файлов в каталог: `cp имя_файла1 имя_файла2 имя_файла3 home/имя_каталога/`.
- Копировать все файлы из каталога: `cp имя_каталога1/* имя_каталога2`.
- Копировать файлы вместе с каталогом: `cp -r имя_каталога1 имя_каталога2`, `имя_каталога1` будет скопировано в `имя_каталога2`.
- Переименовать файл: `mv имя_файла1 имя_файла2`.
- Переименовать каталог: `mv имя_каталога1 имя_каталога2`, если `имя_каталога2` уже существует, `имя_каталога1` будет перемещен внутрь `имя_каталога2`.
- Перемещение нескольких файлов в каталог: `mv имя_файла1 имя_файла2 имя_каталога2`
- Перемещение всех файлов из одного каталога в другой: `mv имя_каталога1/* имя_каталога2`.

## Создание файлов при помощи команд `cat`, `touch`, `gedit` и `vi`

- Используя команду `cat`: `cat > имя_файла`, можно записывать данные в файл `имя_файла`. Горячие клавиши `ctrl + c` позволяют сохранить изменения и выйти из файла. Если файл уже существует, то он перезапишется. Для того, чтобы добавить данные в файл, а не перезаписывать его, нужно использовать оператор добавления `>>`: `cat >> имя_файла`
- Используя команду `touch`: `touch имя_файла`, создастся новый пустой файл. Если файл уже существует, данные перезаписываться не будут, обновится лишь дата последнего изменения.
- Используя команду `gedit`: `gedit имя_файла`. Горячие клавиши: `ctr + s` - сохранить, `ctrl + q` - выйти из графического редактора.
- Используя `vi редактор`: `gedit имя_файла`. Нажмите `i` для входа в режим ввода (insert mode) и `esc`, для выхода из него. Команда `:wq` позволит сохранить изменения и выйти из редактора. `vim` более продвинутая версия `vi редактора`.

## Просмотр содержимого файлов при помощи команд `cat`, `tac`, `rev`, `head` и `tail`

- Используя команду `cat`:  `cat < имя_файла`. Здесь оператор `<` опционален.
- Отобразить содержимое файла с номерами строк `-n`: `cat -n имя_файла1`.
- Отобразить содержимое нескольких файлов: `cat имя_файла1 имя_файла2`.
- Создать и добавить данные в файл: `cat > имя_файла`, ввести данные, нажать `ctrl + d` для выхода из раздела редактирования. Используйте оператор `>>` для того, чтобы добавлять данные в файл.
- Скопировать содержимое одного файла в другой при помощи команды `cat`: `cat имя_файла1 >> имя_файла2`. Использование оператора `>` перепишет содержимое файла `имя_файла2`. 
- Скопировать содержимое нескольких файлов в 1 при помощи команды `cat`: `cat имя_файла1 имя_файла2 >> имя_файла3`
- Отобразить содержимое файла в обратном порядке при помощи команды `tac`: `tac имя_файла`. порядок здесь - это порядок нумерации строк файла.
- Отобразить содержимое файла в обратном порядке по горизонтали при помощи команды `rev`: `rev имя_файла`. Если содержимое файла `имя_файла` будет `Привет!`, то результатом будет `!тевирП`.
Команда `cat` больше подходит для небольших файлов. Если файл большой, то рекомендуется использовать команды `head` и `tail`или `more` и `less`.
- Отобразить первые 10 строк файла: `head имя_файла`.
- Отобразить первые 5 строк: `head -n 5 a.txt` или `head -5 имя_файла`.
- Отобразить все содержиое файла, за исключением последних 5 строк: `head -n -5 имя_файла`.
- Отобразить первые 5 символов содержимого файла: `head -c 5 имя_файла`.
- Отобразить последние 10 строк файла: `tail имя_файла` 
- Отобразить последние 5 строк: `tail -n 5 имя_файла` или `tail -5 имя_файла`.
- Отобразить последние 5 символов содержимого файла: `tail -c 5 имя_файла`.
- Отобразить содержимое файла со строки 3 по строку 7: `head -7 имя_файла | tail -5`

## View files content using less and more
- To view file content page per page:  ```more a.txt```, press ```enter``` to display next line, press ```space bar``` to display the next page, press ```q``` to exit, ```more -d a.txt``` to display more info about the file. By using more command, we can view file content page per page only in forward direction.
- To view file content page per page either in forward direction or backward direction: ```less a.txt```, press ```d``` to display the next page (d means down),  press ```b``` to display the previous page (b means backward).

## Creation of hidden files and directories
- If any file name starts with ```.```, such file is a hidden file.
- Create hidden files: the name of the file should begin by a ```.```, example: ```touch .a.txt```, ```cat > .b.dat```
- Display hidden files: ```ls -a```
- Create hidden directories: ```mkdir .dir1```
- Conversion of Normal/hidden files: using renaiming operation, ```mv .a.txt a.txt```

## Copying moving and renaiming files and directories using cp and mv commands (2)
- ```cp a.txt b.txt```, if b.txt exists, its content will be overwritten directly, to get confirmation message, ```cp -i a.txt b.txt```
- Copy multiple files content to one destination file: ```cat a.txt b.txt > c.txt```
- Moving and renaming files: ```mv oldname.txt newname.txt```
- Moving and renaming directories: ```mv olddirname newdirname```, if olddirname exists already, then olddirname will be moved to newdirname, otherwise the renaming operation will take place.
- Moving selected files to a directory: ```mv a.txt b.txt dir1```
- Moving all files of one directory to another directory: ```mv dir1/* dir2```
- Moving using absolute path:  ```mv ~/dir1/* ~/dir2```, ```~/dir2``` equivalent to ```/home/userName/dir2```


## Comparing content of files (diff sdiff...)
- ```cmp``` command: comparing files byte by byte, ```cmp file1.txt file2.txt```, if the files content are the same, no output, otherwise information about the first found difference, byte number and line number will be shown.
Example:  ```echo "hello" >> file1.txt```, ```echo "hello2" >> file2.txt```, ```cmp file1.txt file2.txt```, output will be ```file1.txt file2.txt differ: char 6, line 1```

- ```diff``` command: it will show all differences, ```diff file1.txt file2.txt```
- ```sdiff``` command: all differences in a parallel comparison.
- ```vimdiff``` command: advanced tool to show the differences, it will highlight all differences in a vim editor, ```sudo apt-get install vim``` to install the tool, two windows will be shown, ```ctrl+w+w``` to go to the other window, ```:q``` to close current window, ```:qa``` to close all windows, ```:qai``` close and ignore all changes. 

##  Soft and hard link
- In Windows, we have only soft link files (shortcut|raccourci), in linux we have also hard link files.
- Hard link file is just another name of the same file. We can create hard link files using the following command ```ln sourcefile.txt hardlinkfile.txt```
- If we deleted the source file, the hard link file wil still exists. If we modify the content of the (sourcefile|link hard file), the update will be reflected also in the (sourcefile|link hard file).
- Soft link file is just a shortcut of the original file (same as windows). If we delete the original file, the soft link file will be broken. We can create soft link files using the following command ```ln -s sourcefile.txt softlinkfile.txt```
- Change made in the original file will also be reflected to the Soft link file.
- For directories, it is not possible to create hard link. 

## Sort commands 
- Sort command, to sort files content line by line in an alphabetical order: ```sort a.txt``` will only print the sorted order. ```sort a.txt > b.txt``` will redirect the sorted order output to the new file. ```sort a.txt > temp.txt``` and ```mv temp.txt > a.txt``` will make change on the same source file.
- Sort in a reverse alphabetical order: ```sort -r a.txt```
- The spaces in the beginning of a line are ignored, blank line came first when sorting, Upper case before lowercase, If the file contains numbers, the numbers will come before letters.
- If we want only unique lines, no duplicate, we should use ```-u``` option, ```sort -u a.txt```
- If we want to sort based on numerical values: ```sort -n a.txt```, ```sort -nr a.txt```
- Sort based on the column line number:  ``` ls etc/ -l | head -7 | sort -rk 5``` will show the info of the top 7 files in etc folder and will sort them recursively based on the fifth column (length of file).
- Sort based on the column lines in a file composed by lines in the following format ```token1:token2:token3```, ```:``` is called a separator. To sort such file: ```sort -k 3 -t ":" a.txt```

## Uniq commands
- Find unique content ```sort -u a.txt```, but uniq command is more powerful, ```uniq a.txt``` works only on sorted files, ```sort a.txt | uniq```.
- With uniq command, we can use multiple options:
  - ```-d```: to display ony duplicate lines.
  - ```-c```: to display numbers of occurrences of each line.
  - ```-i```: to ignore case while comparing.
  - ```-u```: to display ony unique lines.
  
## Input and Output
- command take some input and produces some output:  
  - Input in two forms: stdin or command line argument, stdin example: `echo "hello" >> file.txt`,  command line argument example:  `touch file.txt`
  - Output in two forms: stdout or stderror, stderror in cas when the terminal print arrows.
- Standard Input, Standard Output and Standard Error are data stream and can be redirected from one place to another place. Hence, piping and redirection are possible on those data streams.
    - stdIn associated with the number 0, by default it is connected with the keyboard.
    - stdOutput associated with the number 1, connected with the terminal.
    - stdError associated with the number 2, connected with the terminal.

## Redirecting stdInput stdOutput and stdError
- Redirecting stdOutput: We can perform redirection using `>` and `>>`, `cat 1> output.txt`
- Redirecting standard error: Instead of terminal we can redirect messages from terminal to another place, a file as an example. `cal jkbjkcabjkac 2> log.txt`, 2 stands for stdError.
- Redirecting standard input: we can use the `<` symbol to perform input redirection, `cat 0< a.txt`, 0 is optional.
- Examples:
    - `cat 0<a.txt 1>copy.txt 2>error.txt`
    - `cat <a.txt >copy.txt 2>error.txt`
    - `cat <a.txt &>copy.txt`, means either output or error direction to the copy.txt file.
    - Redirect the documentation content of the ls command to some output file:  ```man ls > newfile.txt```.

## Piping  
- `ls -l /etc | more`, the output of the first command will be the input of the second command.
- `ls -l /etc > somefile.txt | more`, no piping because the redirection symbol breaks the piping.
- `tee` command: if we want to save the output of intermediate command and want to pass that output as input to next command, `ls -l /etc tee somefile.txt | more`
- `rm` command can't take data stream as input, but can only get arguments from the command line terminal, for that purpose, the command `xargs` can be used to converts data stream to arguments. Example: `cat /etc | xargs rm`
- pipe symbol `|` can be used to link two commands, `>` is useful when redirecting the output to another place.

## Execute multiple command
- `ls -l /etc | more`: the preceding commands are dependent commands, to run multiple independent commands in one line, we can use the `;` symbol or by using `&&`.
- By using `;`: e.g. `cmd1;cmd2;cmd3`, if `cmd2` fails, `cmd3` will be executed.
- By using `&&`: e.g. `cmd1&&cmd2&&cmd3`, if `cmd2` fails, `cmd3` will not be executed.

## Commands aliasing
- Aliases are nicknames given to a given command.
- Syntax: `alias nickname="original command name"`, example: `alias cls=clear`. Spaces are not allowed before and after the `=` symbol.
- To list the existed aliases: `alias`, to delete a given alias: `unalias cls`, to delete all aliases `unalias -a`
- To know the original name of an alias: `type cls`
- Aliases are temporary unless we persist them permanently: 
    - Editing the .bashrc file, It could be found inside the user home directory.
    - Create our new aliasing file, the name of the file should be .bash_aliases and should be located in the user home directory.
    
## Regular expressions
- If we want to represent a collection of strings according to a particular pattern, then we should go for 
Regular expressions.
- Some reg expressions rules:
    - \* ----> 0 or more character.
    - ?  ----> 1 character.
    - [abc]  ----> a or b or c.
    - [!abc]  ----> only one character but not a or b or c.
    - [a-z]  ----> any lower case character from a to z.
    - [A-Z]  ----> any upper case character from A to Z.
    - [a-zA-Z] ----> any alphabet from a to z or from A to Z.
    - [0-9]  ----> any digit from 0 to 9.
    - [a-zA-Z0-9]  ----> any of the two above.
    - [!a-zA-Z0-9] ---->  negation of the above.
- Examples: `ls *`, `ls *.*`, `ls *.txt`, `ls a*`, `ls a*t.*`, `ls a?.*`.
    - `ls [abc]*`: aaaaaa, bbbb, ....
    - `ls [!abc]*`: should not start with a, b  or c.

## locate
- We can use locate to locate files and directories in our system.
- `locate file.txt`, `locate *.txt`: to locate the given entries, locate command look in a database to locate the given entries, the database is updated only one time a day, so to update the database we should use the following command: `sudo updatedb`
- `locate -S`: to get the statistics of the database, `locate -i FilE.txt` to ignore case sensitivity. `locate --limit 5 a.txt` to limit the search to 5 entries.
- `locate --existing b.jpeg`, or with `-e` option: check if the given file exist or not.
- Advantage of using a database is related to performance.

## find command
- It provides more search option comparing to the locate command. contrary to the locate command, the find command will search directly in the file system.
- We can search only files, only directories, search by name, search by size...
- `find`: by default, it will look for all files and directories from the current directory and below in the linux file system.
- `find /home`: look for all files and directories from the current directory and below.
- `find -maxdepth 2`: will limit the search only in the 2 levels.
- By default the find command will also look for hidden files.
- `find -type f`: will limit the search to the files.
- `find -type d`: will limit the search to the directories.
- `find . -type f -name d?.*`: look for files inside the current directory and below with the given name that match given regular expression, `-iname` option to ignore case.
- `find . -type f -size +200k`: look for files that have size greater than 200 kbytes, `-size -200k` for less than, `-size 100k` for equality size. 

## Compression and uncompression of files (episode 33)
#### Creation of archive files
- `tar` command: tape archive, to group multiple files and directories into a single archive, `tar -cvf demo.tar file1 file2 dir1`, `-c` create, `-v` verbose,`-f` named file.
- `tar -tvf demo.tar`: print table of content of the tar file.
- `tar -xvf demo.tar`: extract the given tar file.
- `tar -tvzf demo.tgz file1 file2`: will compress and zip the given files.

#### Apply compression algorithm on archive files (gzip bzip2)
- `gzip demo.tar`: To compress a given file, `demo.tar.gz` will be created.
- `gunzip demo.tar.gz`: To decompress a given compressed file. 
- `bzip2` and `bunzip2` as a second alternative to compress and decompress files.
- Archiving and compressing (`gzip`) in one command: using the `-z` option, `tar -czvf demo.tar file1 file2 dir1`
- Decompressing (`gunzip`) and extracting the archive in one command: using the `-x` option, `tar -xvzf demo.tar.gz`

## grep command
- Globally search a regular expression and print it, global regular expression print, global regular expression parser.
- `locate` and `find` help to find required files and directories, `grep` command help to find content within the file.
- Syntax: `grep <pattern> filname`, and it will print all matched lines.
- `grep someword filname1.txt filname2.txt`: look for the pattern in the given files.
- `grep someword *`: look for the pattern in the current directory and not in the sub-directories, to ignore case we should use the `-i` option, `--color` to display the result in a colored form. 
- `grep someword -c *`: to print how much time the pattern is found.
- `grep someword -n *`: to print the lines number where the pattern is found. 
- `grep someword -l *`: to print only the file names where the pattern is found. 
- `grep someword -v *`: to print the lines where the pattern is not found. 
- `grep -w 'word1' *`: will search for the exact word, `aword100` will not be valid, only `word1` will be a correct answer.
- Display before, after and surrounding lines including search result: `-A` means After, `-B` means Before, `-C` means Before and After. `grep 'word1' -B3 *`
- Search multiple contents in a file: `egrep '(word1|word2)' *`, `grep` can understand only some patterns; for this reason we use `egrep`
- `grep -o 'word1' *`: will print only matched pattern.
- `egrep -R '(word1|word2)' *`: will execute recursively, it means also checking the sub-directories.

## Regular expressions patterns
#### Character Patterns
- `grep  'd*' *`: display all lines which contains d followed by any number of characters.
- `grep  'c[aei]b' *`: all lines wich contains `cab`, `ceb` or `cib`
- `grep  'b..x' *`: `.` means any character, it will search for all 4 letter words beginning with b and ending by x.  

#### Word Patterns
- `grep 'linux' demo.txt`: display all lines which contains the word `linux`, for example linuxworld will be valid.
- `grep '\<linux\>' demo.txt`: display all lines which contains exactly `linux`, so linuxworld is invalid.
- `grep '\<linux' demo.txt`: display all lines which starts with `linux`.
- `grep 'linux\>' demo.txt`: display all lines which ends with `linux`.
  
#### Line Patterns
- `^`: line starts with, `grep '^d' demo.txt` will print all lines that start with `d`.
- `$`: line ends with.
- `\<the\>`: lines that start exactly with the word `the`
- `^[aeiu]`: lines that start with `a`, `e`, `i` or `u`
- `^[^aeiu]`: lines that do not start with `a`, `e`, `i` or `u`
- `^....$`: lines that contains only 4 characters.
- `^\.`: lines that starts with the `.` symbol.
- `^$`: blank lines, to remove blank lines, `grep '^$' file.txt > temp.txt`, `mv temp.txt file.txt`.

#### Additional Patterns available only when using the egrep command
- `|`: it matches any of the passed string, `egrep '(linux|java|docker)' *`.
- `{m}`: it matches exactly m occurrences of the preceding character.  `egrep '[0-9]{10}' *` will match every 10-digit mobile numbers.
- `{m, n}`: it matches minimum m occurrences and maximum occurrences of the preceding character.  `egrep '[0-9]{8, 10}' *` will match every 8-digit, 9-digit and 10-digit mobile numbers. `{m, }` means no restriction for the maximum occurrences. 

## The cut command
- we use the cut command to extract specific data from files, the file can be either normal or tabular.
- `cut -c 9 emp.dat`: print the `9th` character in each line.
- `cut -c 3-5 emp.dat`: print the `3th`, `4th`, `5th` character in each line, `-c 3-` the 3th to the last character, `-c -3` will print the `3` first characters by each line.
- `cut -c 3-5 7-9 emp.dat`: will display the `3th`, `4th`, `5th` characters and also the `7th`, `8th` and `9th`
- Display content based on delimiter: `name|username|password`, to print the second column we can use `cut -d "|" -f 3 tabularfile`, `d` option for delimiter and `f` for field, `-f 1-3` to get the columns 1, 2 and 3, `-f -2` to get up to the second column, `-f 1, 3` to get only the first and third column, to get all columns except the third column, we can use  `cut -d "|" --complement -f 3 tabularfile`

## The Linux File Permissions Concept
 File persmmisions describe the allowed operations by various users.
  - User categories.
  - Permission types.
  - Operations allowed related permissions.  

#### User categories
- All users are divided into `4` types:
  - User/owner: represented by `u`, the user who created the file.
  - Group: represented by `g`.
  - Others: represented by `o`.
  - All: represented by `a`.  

#### Permission types
- `r`: Read, on files we can view the content, on directories we can view the content of the directorties; for example `ls` command.
- `w`: Write, on files we can edit the content of files, on directories we can create and delete files.
- `x`: Execute, on files we can execute the file just like a program, on directories we can enter into a directory; for example using `cd` command. Keep in mind to execute a file, both read permission and execute permission are required.
- `-`: No permission.
- By default, the owner of the file get only read and write permissions. 
- Without execute permission, read and write permissions on directories are useless.


#### Operations allowed related permissions
- `+`: add a partcular permission to a `user|group|others|all`.
- `-`: remove a partcular permission from a `user|group|others|all`.
- `-`: assign a set of permissions to a `user|group|others|all`.
- `chmod` command: 
  - It means change mode. we can use it to change files or directories permission.
  - Syntax: `chmod <user_category><permission>`, example: `chmod u+x script.sh`, gives execute permission to the owner on the given file.
  - `chmod u+x,g+w,o-r demo.txt`: gives the owner execute permission, gives write permission to the group and remove read permission from others.
  - `chmod u=rw,g=rw,o=r demo.txt`: we assing read and write permission to the owner and the group, the read opertion to others.
  - `chmod a=- demo.txt`: we retrieve all permissions from all.
  - `chmod a=rwx demo.txt`: we give all permissions to all.
  - `r, w, x` are symbolic permissions, we can also specify permissions by using octal numbers.
    - `0`: `000` means No permission.
    - `1`: `001` means only execute permission.
    - `2`: `010` means only write permission.
    - `3`: `011` means write and execute permission.
    - `4`: `100` means only read permission.
    - `5`: `101` means only read and execute permission.
    - `6`: `110` means only read and write permission.
    - `7`: `111` means read, write and execute permission.
    - Note that `4` means read permmision, `2` means write and `1` means execute.
    - Example:
      - `chmod u=rw,g=wx,o=w demo.txt` could be also written as `chmod 632 demo.txt`.
      - `chmod 77 demo.txt`: is the same thing as `chmod 077 demo.txt`.
      - `chmod demo.txt` is not allowed.

#### Users and groups
  -  `sudo addgroup coursegroup`: to create a group with name `coursegroup`, we can check if the group was added by checking the following file `etc/group`.
  -  `sudo adduser --ingroup coursegroup user1`: to create a new user in the group `coursegroup`. We can check if the user was succefuly added by checking the following file `etc/passwd`.
  -  `sudo adduser user2`: when executing this command, a new user will be created `user2`, a group with the same name will also be created, and the new user will be added to that `group`.
  -  `su - user1`: change current linux user to `user1`.
  
#### Umask
  - umask means user mask. Based on the umask value, default permissions will be there for files and directories. The default umask value is `022`.  
  - Default permissions for files: `666`- umask value, `666`-`022`=`644`, it means read and write for the user, read for the group and the others. 
  - Default permissions for directories: `777`- umask value, `755`-`022`=`644`, it means read, write and execute for the user, read and execute for the group and the others.
  - To congigure ou own umask value, by using the umask command: `umask 002`.
  - Se case:
    - For newly created files, default permission should be `444`, what should be the mask value: `444=666-umask=222`. 
    - The most used umask values are:
      - `022`: `644` on files means read and write for the user, read for the group and others.
      - `002`: `664` on files means read and write for the user and the group, read for the others.
      - `077`: `600` on files means read for the user, nothing for the group and others.
      - `007`: `660` on files means read and write for the user and the group, nothing for others.

## Working with editors
  - There are multiple editors: graphical editor (gedit), vi editor, nano editor... 
  - gedit: same as windows note pad.
    - `gedit file1.txt`: if the file exist already, it will be opened for editing, otherwise a new file will be created and opened for editing. Note that `gedit` can work only on the desktop version.
  - `vi` or `visual editor`: it is a unix based editor, on the contrary to gedit and nano that are linux based. We can use it to create new files and to edit the contrent of the existing ones.
    - `vi file2.txt`: if the file exist already, it will be opened for editing, otherwise a new file will be created and opened for editing.
    - To save the file: `:wq` (w means write, q means quit).
    - There are `3` mode of `vi`:
      - `Command mode`: It is the default mode, in this mode you can use any `vi` command, from command mode we can enter into insert mode by using multiple ways, for example we can use `i`. To enter into exit mode we press `:` key.
      - `Insert mode`: In this mode we can insert/modify/append data, to return to the command mode we can press `Esc` key.
      - `Exit mode`: To insert the exit mode from the command mode, we press `:`, in this mode we can exit the `vi` editor. To return to the command mode we press `Esc`
    - How to insert/append data when we are in the command mode, we can press the following keys:
      - `A`: To append data at the end of the line.
      - `I`: To isert data at the beginning of the line.
      - `a`: To append data to the right side of the cursor position (just after the cursor position).
      - `i`: To insert data to the left side of the cursor position (just before the cursor position).
    - To delete data when we are in the command mode, we can press the following keys:
      - Delete characters and words:
        - `x`: To delete the current character.
        - `nx`: To delete the n characters starting from the current position.
        - `X`: To delete the previous charachter.
        - `nX`: To delete the n previous charachters.
        - `dw`: To delete the current word.
        - `ndw`: To delete the n words starting from the current position.
      - Delete lines:
        - `dd`: To delete the current line.
        - `ndd`: To delete n lines.
        - `d$`: To delete from the current position to the end of line.
        - `d^`: To delete from the beginning to the current position.
        - `dgg`: To delete from the beginning of the file to the current position.
        - `dG`: To delete from the current position to the end of the file.
    - To replace data when we are in the command mode, we can press the following keys: 
      - `r`: To replace the current character.
      - `R`: To replace multiple charatcers from the current position.
      - `S` or `cc`: To replace a line.
      - `O`: To open a new line above te cursor position.
      - `o`: To open a new line below te cursor position.
    - To copy/paste data when we are in the command mode, we can press the following keys:
      - `yy`: To copy one line, `y` for yanking.
      - `nyy`: To copy n lines.
      - `yw`: To copy a word.
      - `nyw`: To copy n words.
      - `y$`: To copy from current cursor to the end of line.
      - `y^`: To copy from the beginning of the line to the cursor position.
      - `p`: small p, To paste below the cursor position.
      - `P`: cpaital P, To paste above the cursor position.
    - Navigation when we are in the command mode:
      - `k`: up.
      - `j`: bottom.
      - `l`: right.
      - `h`: left.
      - Arrow keys can replace the above keys.
      - `$`: go to the end of the current line.
      - `^`: go to the beginning of the current line.
      - `H`: go to the beginning of the current page.
      - `M`: go to the middle of the current page.
      - `L`: go to the end of the current page.
      - `b`: backword, back to the beginning of the word.
      - `nb`: back to the beginning of the nth word.
      - `e`: end of the currentrword.
      - `ne`: end of the third word.
      - `w`: forward, forwarding to the beginning of the next word.
      - `nw`: forward, forwarding to the beginning of the nth next word.
      - `G`: move to the last line.
      - `ctrl+f`: page down.
      - `ctrl+b`: page up.
      - `u`: undo operatio, to undo the previous operation.
    - Exit mode commands:
      - `:w`: save file data.
      - `:wq`: save file data and quit from the editor.
      - `:q`: quit from the editor.
      - `:q!`: ignore changes and quit from the editor.
      - `:set nu`: set line numbers on the editor.
      - `:set nonu`: to remove line numbers from the editor.
      - `:n`: place the cursor to the nth line.
      - `:$`: place the cursor to the laste line.
      - `:!<unix_command>`: to execute any unix command, `:!ls`, `:!date`, ...

## Checking Resource Usage

- `free -m` (memory usage)
- `htop` (cpu usage, live mode)
- `df -mh` (disk space usage)
- `uptime` (how long the system has been running)
- `du -hs /var`: print how much space /var is consuming. 

## Package Management(ubuntu)
- `apt update`: update repository(no instalation)
- `apt list`: list all packages, with `--upgradable` (list only the packages that can be upgraded) 
- `apt search packageName`: to search a given package.
- `apt install packageName`: to install a given package.
- `apt remove packageName`: to remove a given package.
- `apt autoremove`: to remove packages no longer needed/used.
- `apt upgrade`: to upgrades all local packages.
- `apt dist-upgrade`: to upgrades all local packages, even installing new ones or removing existing packeges [more info](https://www.lecoindunet.com/difference-apt-update-upgrade-full-upgrade).


## Managing systemd units
- `systemd` is the process process started by the kernel linux, systemd is responsible for rrunning the other processes, `pstree` to show the processes in a tree structure.
- `ps -ax` to show the processes, the id of `systemd` is 1.
- `systemd` is a system and service manager, it introduces a concept of system units.
- system units are represented by unit configuration files:
  - `/etc/systemd/system/`     -->  managed by admin
  - `/run/systemd/system`      -->  created at runtime.
  - `usr/lib/systemd/system/`  -->  distributed with package installation.
- Types of system units:
  - `service units`
  - `socket units`
  - `path units` 
- `systemctl status jenkins`: systemctl is included in systemd, the preceding command check the status of the jenkins service.
- `systemctl disable jenkins`: do not start jenkins automatically after the boot.
- `systemctl enable jenkins`: start jenkins automatically after the boot.
- `systemctl stop jenkins`: stop the service jenkins.
- `systemctl start jenkins`: start jenkins.
- `systemctl restart jenkins`: restart jenkins.
- `systemctl is-active jenkins`: is the service jenkis active?.
- `systemctl --type=service`: show only service units.
- `systemctl list-dependencies ssh`: show the dependencies of a given service, in other word, what are the other units that will start when starting the given service.
- `systemctl edit --full sshd.service`: to edit the config unit file of the ssh service without the need to know the location of that file in the system.
- `systemctl cat sshd.service`: to print the config unit file. 
- `system show ssh.service`: to print more details about the unit configiguration of that service.
- `systemd analyse blame`: to know how much it took to boot, especially how much every serivice have taken.

## Viewing Logs
- var/log is the location where the logs are persisted, on redhat, different components handle and manage the logs: `syslog`, `syslog-ng`, and `rsyslog`.
- `cat /etc/rsyslog.conf`: to see the configuration of the rsyslog, details about the logs that are managed by rsyslog. 
- `cat var/log/syslog`: print the content of the syslog file. The `var/log` directory contains logs of different services.
- `tail -n 20 var/log/syslog`: print the last 20 lines from the syslog file.
- `tail -f var/log/syslog`: print the last 10 lines from the syslog file, and show any live modification to the output.
- `journalctl -u jenkins`: print only the jenkins service logs, note that we can use also the `-f` option. 
- `journalctl -n 10`: get last 10 entries logs.
- `journalctl -p err`: get error logs.
- `journalctl -p debug`: get debug logs.
- `journalctl -p debug -o json`: get debug logs and convert them to json format.
- `cat var/log/syslog | grep jenkins` print logs that contains the jenkins keyword.
- `cat /etc/logrotate.conf`: print the file content that contains the configuration of the rotation of the logs(removing old entries, ...) 

## Managing users
- `useradd rayan`: to create the new user rayan.
- `usermod -c "rayan bouali" rayan`: update the fullname of the user rayan.
- when a new user created, all the files that exists in `/etc/skel` like `.bashrc` will be copied to the home directory of the new user.
- `id`, `groups`: to know the id of the current user and the groups which the user belong to.
- `cat etc/passwd`: to print the list of users with details like `uis`, `gid`, default bash...
- `cat etc/shadow`: to check the hashed password of the users.
- `cat etc/group`: to print the list of groups.
- `adduser batman`: to add a new user batman.
- `su - batman`: switch to the batman user, logout to come back to the main user. 
- `passwd`: to change the password of the current user.
- `sudo passwd brahim`: to change the password of brahim.
- `sudo userdel -r brahim`: to delete the user brahim, also -r will delete the home directory of brahim.
- `sudo groupadd players`: to add playrs as a new group.
- `groups`: to print the groups where the current user is member.
- `groups zaki`: to print the groups where the user zaki is member.
- `sudo usermod -aG players brahim`: to add brahim to the players group.
- `sudo gpasswd -d zaki players`: to remove the user zaki form the group players.
- `sudo groupdel players`: to delete the grous players.

## SSH
- print actives network connections: `netstat -tulpn`, for pid informations, use `sudo netstat -tulpn` 
- print where the ssh program is lcoated: `which sshd`
- check if ssh is running: `systemctl status ssh`
- to connect to a remote machine via ssh: `ssh username@1.2.3.4` where `1.2.3.4` is the ip adress of the remote machine, the user will be asked to enter the password of the guven user. it is recommended to disallow password authentication and root access to the machine, a better way is to use public/private key authentication.
- `ssh -i publickey.pem username@1.2.3.4` to log in using ssh with the given public key.
- `ssh -v -i publickey.pem username@1.2.3.4` to log in using ssh with the given public key in debug mode, we get more details on the terminal, with that debug mode, if there is some issue to connect via ssh, the output can be helpful.
- `ssh -p 33 username@1.2.3.4`: to connect via ssh on a customized port, normally the default port is `22`.
- default configuration of ssh in the server: `/etc/ssh/sshd_config`. 
- to check the logs of authentication to the server: `/var/log/auth.log`.
- on the client side, when connecting via `ssh` to a remote server, a folder named `.ssh` will be created and will contains the following files:
  - `known_hosts`: hosts that the client already connected to via `ssh`.
  - `id_rsa`: private key.
  - `id_rsa.pub`: public key.
- ssh server configuration: 
  - the config file for ssh server to edit is `/etc/sshd_config`, the config for the client ssh is `/etc/ssh_config`.
  - we can edit some configurations like port number, prohibit root login, no user/password authentication....
  - We can allow only some users or groups to connect via ssh with `AllowsUsers groupname user1 user2`
- keys generation:
  - ssh-key-gen: to generate new keys, by default they will be placed inside `.ssh` folder, `id_rsa` as default name of the private key, `id_rsa.pub` as default public key name, the private key should be kept private.
- `ssh-copy-id -i /.ssh/id_rsa.pub username@1.2.3.4`: to copy the public to the remote ssh server, with that further logging will succeed without passing password or publickey. 
- `ssh-copy-id` will copy our public key to the remote `/.ssh/authorized_keys` file in the ssh server. In the authorized_keys file, every line represent a client ssh public key.
- `ssh root@1.1.1.1 ls /etc`: will run the command directly `ls /etc` on the remote server throught ssh without the need to get to a shell, we can use the option `-t` if there is a need for a terminal, example using vim editor. 
- `last`, `lastb`, : to check last logging activities, `last` for successful logging, `lastb` for bad logging.
- `man sshd_config`: for the man page of the sshd_config file.
- `scp EffectiveJava3rd.pptx azureuser@20.127.10.12:`: to copy the given file to a remote machine using scp.

## Bash history
- `history`: to print history of typed commands, every command will have an number associated.
 we can run the `command with number 10` by typing `!10`.
- to not save typed commands on the history, we type a space before typing the command name. 

## Process control commands

### Types of processes
- user process: started by a regular user, they run in the user space. a user process dosen't have special access to the cpu/files that dosen't belongs to him.
- daemon process:
  - designed to run in background, it manages some ongoing service, like sshd, httpd.
  - Generally they are managed by the user root. But tey run as non root user for security reasons, there is a dedicated user account for those types of processes, like sshd for the service sshd...
  - They are often started automatically and shutdown when the system is stoped.
  - They can be started and stoped on demand. 
- Kenrel process: 
  - similar to daemon process, but they run in kernel space.
  - kernel process have access to kernel data structure which made them powerful.
  - dificult to change the behaviour of the kernel process, for the daemon it is possible to change its behaviour by adapting the configuration files. 

### background/foreground mode
- run a process in background mode: `man ls &`, the man program will run in the background mode, we can also send a process to bakground by typing `ctrl+z` when it is in a running mode.
- to see how many jobs we have (background running process): `jobs`
- to return a background process to the foreground: `fg` without parameters, automatically the job with `+` sign will be brought to the background, we can also pass the identifier of a process.

### ps command:
- `ps -e`: print all running processes.
- `ps -f`: print all running processes with full details.
- `ps -aef | grep ls`: to get info about a specific process.
- `ps -p 1`: to get info about a process based on a given PID.
- `ps -u zaki`: to get info about a process based on a given UID.

- `pstree`: to print the tree of the processes.
- `pidof firfox`: to print the id of the process firfox.
- `nice`: to change the priority of a given process, `nice -n 10 vim /etc/passwd` run the vim process with a priority equal to 10.
- a priority of a process range from -20(highest priority) to 19 (the lowest priority).  

### top command:
- `top` command will display the complete active process, cpu and memory information, `shift+p` will order the output based on cpu usage, `shift+m` will order based on memory usage, `c` to print the absolute path of the process, `k` to kill a process.
-  `top -u zaki`: print only processes owned by a given user.

### kill command:
- `kill 1245` kill the process with the pid 1234, you should be able to kill a process only if youa are the owner of that process.
- `kill -9 5678`: forcing to kill the process with sigkill signal.
- `killall vim`: killing all the vim process.
- `kill -l`: print all the signals that we can use to kill a process.

## Network linux commands
- ip adress classes:
![image](https://user-images.githubusercontent.com/34305250/155011424-5be7d7b0-fea4-437d-8e5c-094655422281.png)

- `hostname`: to print the name of the host, with `-d` option it prints the domain name which the machine belongs to, with `-f` option, it prints the fully qualified domaine name, with -`i`, it prints the ip address of the machine.
- `ping`: used to cchechk the establishement of the connection and also the speed of that connection, `ping www.google.fr`.
- `netstat`: list detailed information about connection to and from the host, with `-t` option we list only tcp connections, with u only udp connections and with `-l` we list only listening ports, with -p we list also the pid/program name information.
- `netstat -c`: display information continiously (live)
- `netstat -r`: display the kernel routing table.
- `netstat -ap | grep ssh`: check on which port ssh is running
- `netstat -s`: print connection statistics.
- `netstat -lx`: print all unix listening ports.
- `netstat -i`: show network interfaces, with -e, more extended output.
- `ifconfig -a`: view all network configuration & setting.
- `ifconfig eth0`: to view specific network setting.
- `ifconfig eth0 up`: enabling eth0 interface.
- `ifconfig eth0 down`: disabling eth0 interface.
- `nslookup`: to get ip address from dns name or vise-virsa: `nslookup www.google.fr`.
- `traceroute`: utility to view the number of hopes to reach a given host.
- `ip addr show`: print the network interfaces datails, `ip a s` for the abreviated command.
- `route -n`: print the routing table.
- `nmcli connection show`: to print the details of the connections.

## [man page](#man-page)
- man is the builtin help system in Linux, man is short for manual, a man page is a documentation.
- `man man`: to see the man page of the man command.
- when on the man page we can type:
  - `h` for displaying help, `q` to quit.
  - `y` to go backward one line.
  - `b` backward one window. 
  - `g` go to the first line. 
  - `G` go to the last line. 
- searching :
  - by typing `/keyword`: search the keyword forward in the page.
  - by typing `?keyword`: search the keyword backward in the page, type `n` to go to next found keyword, `N` in the reverse order.
- `ls` man page:
  - Synopsis: `ls [OPTION]... [FILE]...` : means that we can pass many optional option and many optional file to the `ls` command.
- `man -k ls`: search the manual page name for the keyword `ls`.
- `man 2 mkdir`: open the sectioné of the man page of the mkdir command.
- The man-pages manual describes the convention that should be employed when writing man pages.
- some shell commands(built-in shell commands) don't have a specific man page, we can use help to get more details, for example `help while` to get details about the while shell keyword.
- we can get brief help for a given command by passing `--help` option, `ls --help` will output details about the `ls` command.

## curl command
- curl is a tool to transfert data between from or to server using one of the supported protocols.
- curl www.google.fr 
- curl -i www.google.fr: extra information (headers).
- curl -d "data inside the body post request" www.google.fr: post request.
- curl -X PUT -d "data inside the body post request" www.google.fr: put request.
- curl -X DELETE google.fr: to send a delet request.
- curl -u username:password needauthentication.com.
- curl -o resp1.txt www.google.fr : to save the response received to the resp1 file.


## Stackoverflow questions
- [What is the difference between ps and top command?](https://unix.stackexchange.com/questions/62176/what-is-the-difference-between-ps-and-top-command)


# Shell scripting
## What is Shell?
  - Shell is responsible to read the command provided by the user.
  - Shell will check if the command is valid or not.
  - Shell will check if the command is properly used or not.
  - If everything is ok, the shell will interpret that command into kernel understandable form and pass that command to the kernel. The kernel is responsible to excute that command with the help of the hardware.
## Types of Shell?
  - `Bourne Shell`: was developed by `Stephen Bourne`, it came with the first version of `Unix`. By using `sh` command we can access this Shell.
  - `Bash Shell`:    Bash for Bourne Again SHell. It is an advanced version of Bourne Shell (sh), this is the default Shell for the most linux distributions, by using `bash` command, we can access this Shell.
  - `Korn Shell`: developed by David Korn, mostly used in IBM AIX OS, by using `ksh` command, we can access this Shell.
  - `Cshell`, `TShell`,`ZShell`, ...
## Scripts and Shell info
  - To cretae a script, we can create a file named myscript.sh, we can add commands into it.
  - To execute the script, we should give the user execute permission on the given script, and we run the script using `./myscript.sh`, note that wen executing the preceding command , the defaut shell will be executed (Bash Shell), to use `Bourne Shell` for example, we can type `sh ./myscript.sh`.
  - How to check default shell in our sysrtem: `echo $0`, or `echo $SHELL`, not that LINUX IS CASE SENSITIVE, we can also check for this info by checking the following file `cat /etc/paswd`; this file contains the configuration of the system users. 
  - How to check all available shell in our system: `cat /etc/shells`
  - To switch from one shell to another: we type `sh` to switch to the `sh` shell.
  - What is a shell script: a sequence of commands and programming features saved in a file. the programming features like control statement, loops, ...
  - Executing a script using the bash shell: `/bin/bash /home/zaki/myscript.sh`, we can use directly the `bash` command if it can be found inside a location that exists in `$PATH` variables. If the `myscript.sh` file exists in the same directory as the user, we can run it with `bash ./myscript.sh` or `./myscript.sh` if the `bash` is the default Shell in the system. If we want to use the `sh` Shell, ` sh ./myscript.sh`
  - Inside a script file, we can specify the interpreter, which is responsible to execute the script. We can do that using Sha-Bang `#!`, for example: adding `#! /bin/sh` in the first file of the script to specifiy the `sh` shell.
  - By default, for any command or script, the OS will check locations specified by the `$PATH` varaiable. So if we add our scipt location to path variable locations, we can then run the script from anywhere just like a command.
  - `EXPORT PATH=$PATH:/home/user/scripts`: will append the new location (`/home/user/scripts`) to the PATH variables, not that the result of this operation is temporary and available only at session level.
  - To set the PATH permanently at a user level: we should add `EXPORT PATH=$PATH:/home/user/scripts` to the hidden file `.bashrc`, so whenever a new session begin (session means a new command line terminal opening operation), the `.bashrc` file will executed and the path will be adjusted.
## Variables in Shell programming
  - In Shell programming, we don't have the notion of data types, every value is text or String type.
  - All variavbles are divided into two type:
    - Predifined variables (environement variables).
    - User defined variables 

#### Predifined variables (environement variables)
  - They are mostly used by the system internally, but we can use them in our script. we can get all environement variables either using `env` or `set`
  - Demo SCRIPT usING environement variables:
      ```
      echo "user Name: $USER"
      echo "USER HOME directory: $HOME"
      ```
#### User defined variables 
  ##### variables name
  - It is recommanded to use only upper case characters.
  - If a variable name is composed by multple words, it should be separated with the `_` symbol.
  - Should not begin with digit.
  - We should not use special symbols: `-`, `@`, `#`, `$`, ...

`readonly A`: To define a variable `A` as readonly. 


#### variable scopes
  - There are 3 scopes available for variables:
    - Session scope.
    - User scope.
    - System scope.
  - Session scope: variables declared in the terminal are said to be session scope, once we close the terminal, all those variables are gone.
  - User scope: for each user, there is a special file `.bashrc`, variables declared inside this file are available for that user in every session. user scoped variables are not available to other users.
  - System scope: the variables are availbe to all users of the system. To declare system scoped variable, we can declare them inside the following file `/etc/profile`. Example: `export global_variable=globalValue`, to validate the changes of the system scope variables we should restart the OS.

#### Variable substitution
- Accessing the value of a variable by using the $ symbol is called variable substitution.
- Syntax: `$variableName` or `${variableName}herewecanappendsomething`
- Example:
  ```
  name=zaki
  echo $name
  echo "${name}"
  ```
  Note that echo `$name` will not work as expected, and the variable substitution will not work.

#### Command substitution  
- Command substitution means execute command and substitute its result.
- Example:
  ```
  currentDate=$(date)
  echo $currentDate
  ```
  Or using the old way
  ```
  currentDate=`date`
  echo $currentDate
  ```
- We use command substitution whenever we need to use the result of a linux command. Example: `echo "the current working directory is $(pwd)"` 

#### Command Line arguments
- To run a specified script with arguments: `./script.sh hello world, It is friday`
- inside the script, we can get:
  - The numbers of arguments: `$#`
  - The script name: `$0`
  - The first argument: `$1`
  - The second argument: `$2`
  - All arguments: `$*` or `$@`.
  - With `$@`, we get space between each two argments `$1` `$2`, with `$*` we get special character between each two characters `$1c$2`, the c is the first character in the IFS(Internal Field Separator), the default is tha space charcter.
  - To check default IFS: `set | grep "IFS"`
- `echo -n "APPLE" | wc -c` Vs  `echo "APPLE" | wc -c`
- Example using variable/command substituion and a command line arguments
 ```
      echo "hello"
      len=$(echo -n $1 | wc -c)
      echo "the lengh of the given parameter is $len"
 ```

#### Read dynamic data from the user
- Without prompt message: `read a b`, to read two values from the user. 
- With prompt message: 
```
      echo "Enter the first value"
      read A
      echo "Enter the second value"
      read B
      echo "A is $A"
      echo "B is $B"
 ```
 - In place of the above code, we can use the following approach: `read -p "enter the first value:" A`, the entered value will be stored to the A variable.
 - The `-p` for displaying message, `-s` to hide the user input. `read -s -p "enter the password value:" pass`, note that the `-s` should be provided before the `-p` option.
 - Write a script that read a file name from the user, and remove bank lines from that file?
  ```
        read -p "Enter the file name:" filename
        grep -v "^$" $filename > temp.txt
        mv temp.txt $filename 
  ```
 - Write a script that read a file name from the user, and remove duplicate lines from that file?
  ```
        read -p "Enter the file name:" filename
        sort -u $filename > temp.txt
        mv temp.txt $filename 
  ```
#### Operators
  - Arithmetc operators: `+ - * / %`
  - Relational operators (numeric comparison operators), they return boolean value:
    - `gt`: greatet than.
    - `ge`: greatet than or equal.
    - `lt`: less than.
    - `let`: less than or equal.
    - `et`: equal to. 
    - `gt`: Not equal to.
  - Logical operators:
    - `a`: Logival AND
    - `o`: Logival OR
    - `!`: Logival NOT
#### How to perform matematical operations
  - There are multiple ways to perform matematical operations.
  - ##### By using expr keyword
     - `sum=` `expr $a + $n`  
     - `sum=$(expr $a + $n)`  
     - Both the  `$` symbol and the space are mandatory.
  
  - ##### By using let keyword
     - Most used approach.
     - `let sum=$a+$b`
     - The `$` symbol is optional, we should not put space before or after the `+` symbol.

  - ##### By using (())
     - `sum=$(($a + $n))`   
     - Both the  `$` symbol and the space are optional.

  - ##### By using []
     - `sum=$[$a + $n]`   
     - Both the  `$` symbol and the space are optional.

  - All the above approaches will work only for integer arithmetic operations, for floating point calculations we should use the `bc` command. 
  - `bc` command for binary calulator. From the terminal we can start using the bc command.
  ```
    read -p "enter the first floating number" a
    read -p "enter the second floating number" b
    sum=$(echo $a+$b | bc)
    echo "the sum is $sum"
  ```
  - Write a script to sum read 4 given digits:
   ```
      read -p "Enter any 4 digits without space" n
      a=$(echo $n | cut -c 1)
      b=$(echo $n | cut -c 2)
      c=$(echo $n | cut -c 3)
      d=$(echo $n | cut -c 4)
      sum=$[a+b+c+d]
      echo "the sum is $sum"
   ```

#### Control statements

##### if statement
- Simple if statement: 
  - Syntax:
    ```
            if [ condition ]
            then
              action
            fi
    ```
  - Example: read a name from the user
    ```
            read -p "enter your name :" name
            if [ $name = "Sunny" ]
            then
              echo "Your name is Sunny"
            fi
    ```

  - Note that the instruction `a=b` is an assignement and `a = b` is a comparison instruction, also the spaces between `[]` are mandatory. 
- if else  statement: 
  - Syntax:
    ```
            if [ condition ]
            then
              action1
            else
              action2
            fi
    ```
  - Example: read a name from the user
    ```
            read -p "enter your name :" name
            if [ $name = "Sunny" ]
            then
              echo "Your name is Sunny"
            else
              echo "Your name is not Sunny"
            fi
    ```
- Nested if statement: 
  - Syntax:
    ```
            if [ condition1 ]
            then
              if [ nestedcondition ]
              then
                action1
              else
                action2
            else
              action3
            fi
    ```
- Ladder if statement: 
  - Syntax:
    ```
            if [ condition1 ]
            then
              action1
            elif [ condition2 ]
            then
              action2
            elif [ condition3 ]
            then
              action3
            fi
    ```
  - Example: read a name from the user
    ```
            read -p "enter your name :" name
            if [ $name = "Sunny" ]
            then
              echo "Your name is Sunny"
            elif [ $name = "Bunny" ]
            then
              echo "Your name is Bunny"
            else
              echo "Your name is unknown"
            fi
    ```
- Question1: Write a script to find the greater of two numbers:
    ```
      read -p "Enter the first number" a
      read -p "Enter the second number" b
      if [ $a -gt $b ]
      then
        echo "the first number is greater than the second"
      elif [ $a -lt $b ]
      then
        echo "the second number is greater than the first"  
      else
        echo "the first number is equal to the the second"  
      fi  
    ```
- Question2: Write a script to find the greanter of three numbers:
    ```
      read -p "Enter the first number" a
      read -p "Enter the second number" b
      read -p "Enter the third number" c
      if [ $a -gt $b -a $a -gt $c ]
      then
        echo "the first number is the biggest"
      elif [ $b -gt $c ]
      then
        echo "the second number is the biggest"  
      else
        echo "the third number is the biggest"  
      fi  
    ```
    - Note the use of the `-a` in the first condition, it perfroms the `AND` logical operation, `-o` for the logical or operation, `!` for logical not.

- Question3: Write a script to find if a given number is even or not:
    ```
      read -p "Enter the first number" a
      if [ $[a%2] -eq 0 ]
      then
        echo "Yes it is even"
      else
        echo "No, it is not"  
      fi  
    ```
##### Exit codes / Status codes
- Every command return some value after execution, This returned value is the exit code or status code, we can find exit code by using the `$` symbol.
- The status code value have a range between `0` and `255`, the value `0` means that the command/script executed successfuly, otherwise not.
- Example:
  ```
    rm inexistentfile
    echo $?
  ```
  - The above code will print `1`, as the command `rm` didn't execute successfuly.

- Exit command: useful when there is a need to exit in the middle of an execution script. 
  - Syntax: `exit status-code`
   
##### File test options
- The `-e` option return true if a given file/directory exists.
- Script to test if a file exists in the current working directory:
   ```
    read -p "enter file name to test" name
    if [ -e $name ]
      echo "exists"
    else  
      echo "does not exist"
    fi  
   ```
- The `-f` option returns true if a given file is a regular file.
- The `-d` option returns true if a given file is a directory.
- The `-s` option returns true if a given file is not empty, `-s` for size.
- The `-l` option returns true if a given file is a link file.
- The `-b` option returns true if a given file is a block special file.
- The `-c` option returns true if a given file is a character special file.
- The `-r` option returns true if the current user has read permiision on the given file.
- The `-w` option returns true if the current user has write permiision on the given file.
- The `-x` option returns true if the current user has execute permiision on the given file.
- The `-o` option returns true if the current user is the owner of the given file.
- `file1 -ot file2` returns true if `file1` is oltder than `file2` (last modified time).
- `file1 -nt file2` returns true if `file1` is newer than `file2` (last modified time).
- The `-z` option returns true if a given string is empty.
- Examples:
  - Write a script to test whether a given file is regular file or directory:
    ``` 
    #! /bin/bash
    read -p "enter file name to test" name
    if [ -e $name ]
    then
      if [ -f $name ]
      then
        echo "it exists and it is a regular file"
      elif [-d $name ]  
        echo "it exists and it is is a directory"
      else
        echo "it is something else"
      fi  
    else
      echo "does not exist"
    fi  
      ``` 
  - Write script to comapre two files    
    ``` 
      read -p "enter the first file name" file1
      read -p "enter the second file name" file2
      result=$(cmp $file1 $file2)
      if [ -z "$result" ] then
        echo "they are same"
      else  
        echo "they are not"
      fi
    ``` 
##### String test options    
- `str1 = str2` returns true if both strings are equal.
- `str1 != str2` returns true if both strings are not equal.
- `-z` str1 returns true if `str1` is empty.
- `-n` str1 returns true if `str1` is not empty.
- `str1 > str2` returns true if `str1` is alphabitically greater than `str2`.
- `str1 < str2` returns true if `str1` is alphabitically lesser than `str2`.
- Note that the symbol `<` is also a redirection symbol, so we should use the backslach `str1 \< str2` 
- `[ 0 ]`, `[ 1 ]` returns true all the time.
- Script to test if the logged user is root or not and provide 5 current rnning processes information:
  ```
  user=$(whoami)
  if [ $user = "root" ]
    echo "you are root"
    ps -ef | head -6
  else
    echo "you are not root"
  ```
  `ps` for process status, `-e` every process, `-f` full listing.

##### case statement
- Syntax:
    ``` 
      case $variable in 
        option1)
              action-1
              ;;
        option2 )
              action-2
              ;;
        optionn)
              action-n
              ;;
        *)
              default action
              ;;
      esac         
    ```   
- The space in `option2 )` is optional, `;;` is used to break from the case statement, it is optional in the default option. It is recommended if you use the default statement to put it as a last step in the case statement.    

- Write a script to read a digit from 0 to 5 and print its string equivalent in the console using the case statement:
  ```
   #! /bin/bash
   read -p "enter any digit from 0 to 9" digit 
   case $digit
    0)
      echo "zero"
      ;;
    1)
      echo "one"
      ;;
    2)
      echo "two"
      ;;
    3)
      echo "three"
      ;;
    4)
      echo "four"
      ;;
    5)
      echo "five"
      ;;
    *)
      echo "please enter a number between 0 and five"
   esac   
  ```
  For string case statement:
  ```
      case $String
        "AL")
          echo "zero"
          ;;
        "BL")
          echo "one"
          ;;
  ```
  Using regular expressions:
  ```
      case $Character
        [abc])
          echo "a, b or c"
          ;;
        [^abc])
          echo "any character except a and b and c"
          ;;
        [a-z])
          echo "any lower case character"
          ;;
        [A-Z])
          echo "any upper case character"
          ;;
        [a-zA-Z])
          echo "any alphabet character"
          ;;
        [0-9])
          echo "any digit from 0 to 9"
          ;;
        [a-zA-Z0-9])
          echo "any alphanumeric character"
          ;;
        [^a-zA-Z0-9])
          echo "any character except alphanumeric character"
          ;;            
  ```
##### while loop
  - Syntax
      ```    
        while [ condition ]
        do
          body
        done  
      ```

  - Write a script to print numbers from 0 to 9:
     ``` 
        #! /bin/bash
        i=0   
        while [ $i -le 9 ]
        do
          echo $i
          sleep 2          
          let i++
        done  
      ```
    `let i++` could also be written as `i=$[i+1]`, `sleep 2` for sleeping two seconds.
  - Write a script to display time every second:
     ``` 
      while [ true ] 
      do
        clear
        echo -e "\n\n\n\n$(date +%H:%M:%S)"
        sleep 1
      done
     ```  
    The -e option to process the scape characters like `\n`, we can replace `echo -e` by `printf "\n\n\n\n$(date +%H:%M:%S)"`
    
    To put the cursor in some position, we can use the following command `tput cup x y` where `x` and `y` are the row and the column numbers respectivly.  
##### break and continue
- To break the loop execution
    ``` 
      i=1
      while [ $i -le 10 ] 
      do
        if [ $i -eq 5 ]
        then 
          break
        fi  
        clear
        echo "$i"
        let i++
      done
     ```
- To skip the current iteration and continue for the next iteration
    ``` 
      i=1
      while [ $i -le 10 ] 
      do
        if [ $i -eq 5 ]
        then 
          continue
        fi  
        clear
        echo "$i"
        let i++
      done
     ```  
- Write a script to reverse a given string
    ```  
      read -p "please enter a String: " word
      length=$(echo -n $word | wc -c)
      output=""
      while [ $length -ge 1 ]
      do
        lastcharcter=$(echo -n word | cut -c $length)
        output=$output$lastcharacter
        let length--
      done
      echo "the reversed character $output"  
    ```  
- Write a script to read a file line by line
    ```  
      read -p "please enter the file name: " fname
      if [ ! -e $fname ]
      then
        echo "the file dosn't exist"    
        exit 1
      fi  
      if [ -d $fname ]
      then
        echo "it is a directory, and not a file"    
        exit 2
      fi
      if [ ! -s $fname ]
      then
        echo "it is empty"    
        exit 3
      fi
      count=1
      while read line
      do
        echo "   $count  $line"
        let count++
      done < $fname
    ```  

##### for loop
  - Syntax
     ```    
        for variable in item1 item2 item3... itemN
        do
          action
        done  
     ```
  - Print numbers from 1 to five
     ```    
        for i in 1 2 3 4 5
        do
          echo "$i"
        done  
     ```
  - Print every number from 1 to 100 that is divisible by 10
     ```    
        for i in {1..100}
        do
          if [ $[i%10] -eq 0 ]
          then
            echo "$i"
          fi  
        done  
     ``` 
  - Display all file names present in the current working directory
    ```
      #! /bin/bash
      for fname in *
      do
        if [ -f $fname ]
        then
          echo "$fname"
        fi  
      done
    ```
  - Diplay the command line arguments passed to the script 
    ```
      #! /bin/bash
      if [ $# -eq 0 ]
      then
        echo "no arguments"
        exit 1
      fi  
      for arg in $@
      do
        echo "$arg"
      done
    ``` 
  - Diplay the third value of each row of the following file
    ```
        100:anny:1250:A
        200:bnny:2250:B
        300:snny:3250:C
    ```
    ```
        #! /bin/bash
        for row in $(cat abovefile.txt)
        do
          value=$(echo $row | cut -d ":" -f 3)
          echo value
        done
    ``` 
    ##### alternative syntax of for loop
    ```
        #! /bin/bash
        for ((i=0; $i<5; i++))
        do
          echo $i
        done  
    ```
    - Inside the expression ((...)), the spaces and the $ symbol are not required.
    - Write a script to test if a number is prime
    ```
        #! /bin/bash
        read -p "enter a number grater than 1" n
        counter=0
        for ((i=2; $i<=n/2; i++))
        do
          if [ $[n%i] -eq 0 ]
          then
            echo "it is not a prime number"
            exit 1
          fi  
        done  
        echo "it is a prime number"
    ``` 

#### Arrays concept
##### How to create arrays
- If we know elements at the beginning: `courses=("java" "shell" "linux")`
- If we don't know elements at the beginning: `courses[0]="java"`, `courses[1]="shell"`, we are not required to declare the courses array separately, but we can do it using the follwing code `declare -a courses`. The index values need not be consecutive, we can take randomly.

##### How to access arrays
- We can access array elements by using index which is 0 based.
- `echo ${courses[0]}` will print the first element of the array.
- `echo ${courses[@]}` will print all elements of the array with space separator.
- `echo ${courses[*]}` will print all elements of the array spaced with [IFS](https://github.com/JavaZakariae/Linux-command#command-line-arguments).
- `echo ${!courses[@]}` will print all indices where elements are available.
- `echo ${#courses[@]}` will print the number of elements present inside the array.
- `echo ${#courses[0]}` will print the length of the first element. 
##### Examples
- Write a script to create an array with some elements and print all its elements by using while loop, for loop and the alternative for loop
  - Using while loop
  ```
        #! /bin/bash
        declare -a fruits
        fruits={"A", "B", "C"}
        index=0
        while [ index -lt ${#fruits[@]} ]
        do
          echo ${fruits[$index]} 
          let index++
        done  
  ```
  - Using for loop
  ```
        #! /bin/bash
        declare -a fruits
        fruits={"A", "B", "C"}
        for fruit in ${fruits[@]}
        do
          echo ${fruit} 
        done  
  ```
  - Using alternative for loop
  ```
        #! /bin/bash
        declare -a fruits
        fruits={"A", "B", "C"}
        for((index=0; index<${#fruits[@]; index++))
        do
          echo ${fruits[index]} 
        done  
  ```
#### Shell Script Functions
##### How to define a function 
  - First way
    ``` 
      function f1()
      {
          a=$1
          b=$2
          echo "you passed $a and $b" 
      } 
    ```
  - We call the function by the flllowing command `f1 5 6`
  - The function keyword is optional, if we need to pass parameters, it is not possible to declare them in the function signature, but we can access them using `$1` for the first parameter, `$2` second, ...
  - Write a function that print all passed parameters:
    ```
    #! /bin/bash
    shellfunction()
    {
        if [ $# -eq 0 ]
        then
          echo "please you should pass parameter to the function"
        else
          for param in $@
          do
            echo $param
          done
        fi    
    }
    # calling the above function
    shellfunction 1 254 4
    ```
  - Write a function that print the factorial of a given integer number:
    ```
    #! /bin/bash
    factorial(){
      if [ $1 -le 0 ]
      then
        echo "please enter a positive integer"
      else
        let factorial=1;
        for ((let i=2; i<$1; i++))  
        do
          factorial=$factorial*i
        done
        echo $factorial
    }
    read -p "enter any positive integer" n
    factorial $n
    ```
##### Varibale scopes 
  - The below examples are valid programs, by default every declared variable has a global scope, even those declared inside a function. Before using a variable, it should be declared already. 
    ```
      #! /bin/bash
      f1(){
        echo $x
      }
      x=10
      f1
    ```

    ```
      #! /bin/bash
      f1(){
        x=10
      }
      echo $x
      f1
    ```
  - If we want to declare a variable local to a function, we use the `local` keyword.
    ```
        #! /bin/bash
        f1(){
          local x=10
        }
        f1
        echo $x  #no access to the x variable, en empty value will be printed.
    ```

    ```
        #! /bin/bash
        f1(){
          local x=10
        }
        f1
        x=20
        echo $x   #will print 20.
    ```
##### Return statement
  - Every function in shell scripting returns some value, the dafault return value is the exit code/status code of the last command inside function. But based on our requirement, we can return values explicitly by using the return statement `return <exit_code>`, the allowed values are in the range `[0, 255]`. we can get the return value of the function bu using `$?`.
  - The difference between `exit` and `return` in context of a function, the `exit` will end the program, but `return` will only returns from the function and the program can continue executing.       
##### break vs exit vs return
  - break: we can use break only inside loops to break loop execution.
  - exit: we can use exit anywhere, to terminate script execution.
  - return: we can use return only inside function to stop the execution of the function.
##### How to call functions present in another script
  `utilistyscript.sh`
  ```
        #! /bin/bash
        add()
        {
          echo "$1 + $2= $[$1+$2]"
        }
  ```
 `main.sh`
  ```
        #! /bin/bash
        . ./utilistyscript.sh 
        add 5 10
  ```
  the line `. ./utilistyscript.sh` for including the script `utilistyscript.sh`, the script should be placed in the given path.
  
  
## Various topics
- Hox to copy files over ssh: [awnser](https://unix.stackexchange.com/questions/106480/how-to-copy-files-from-one-machine-to-another-using-ssh)
