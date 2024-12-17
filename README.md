## 1.Использование команды grep для поиска текста
Простое задание с пошаговым объяснением:
Использовать команду `grep` для поиска строк, содержащих слово "error" (регистр игнорировать), в лог-файле `system.log`
Grep это утилита командной строки Linux, который даёт пользователям возможность вести поиск строки. С его помощью можно даже искать конкретные слова в файле. Также можно передать вывод любой команды в grep, что сильно упрощает работу во время поиска и траблшутинга.
## Шаги выполнения:

## 1.Подготовка данных:
Создайте файл `system.log` и добавьте в него тестовые данные:
```
echo -e "Info: System started\nError: Disk full\nWarning: Low memory\nerror: Connection lost" > system.log
```
## 2.Запустите поиск с учетом регистра:
Выполните команду:
```
grep "error" system.log
```
Вывод будет содержать только строку `error: Connection lost.`
## 3.Добавьте флаг `-i` для игнорирования регистра:
```
grep -i "error" system.log
```
Теперь в выводе будут строки с `Error: Disk full и error: Connection lost.`
## 4.Используйте флаг `--color` для подсветки:
```
grep -i --color "error" system.log
```
## 5.Примените флаг `-v` для исключения строк с "error":
```
grep -v -i "error" system.log
```
Вывод: строки без слова "error".


## 2. Задача на выполнение
# Задание:
Если же нужно найти не одно слово, а словосочетание или целое предложение, то параметр команды grep должно быть выделено кавычками. Grep поддерживает как одинарные, так и двойные кавычки.
Найти в каталоге все файлы, содержащие слово "dog", и подсчитать количество таких строк. Подготовить каталог с файлами для теста.

Подсказка: Используйте параметры `-r`, `-c` и комбинируйте их.

Ожидаемый результат:

Количество строк с "dog" в каждом файле.
Подсветка найденного текста.
Пример команды:
```
grep -r --color -c "dog" my_project/
```
## Ссылки на материалы:

https://wiki.merionet.ru/articles/rukovodstvo-po-komande-grep-v-linux

https://selectel.ru/blog/tutorials/grep-command-in-linux/

## Решение 
1.Использование команды grep для поиска текста
Простое задание с пошаговым объяснением: 
<img width="556" alt="Снимок экрана 2024-12-17 в 18 43 45" src="https://github.com/user-attachments/assets/d0797a4d-5725-4ba4-ba7f-bd81a56b06e0" />
<img width="790" alt="Снимок экрана 2024-12-17 в 18 44 24" src="https://github.com/user-attachments/assets/0067bf24-d95d-4b11-9d30-d65f78f6a7c5" />

2. Задача на выполнение
<img width="637" alt="Снимок экрана 2024-12-17 в 19 18 17" src="https://github.com/user-attachments/assets/d8522ce1-92a8-4814-810b-5fbcc8c4f065" />

