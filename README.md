# git_bash
## Работа с git и bash
Задача 1:
    1. Предварительно создайте файл bash1.txt, в который вы будете добавлять выполненные команды.
    2. Открыть домашнюю директорию через терминал
    3. Определить имя папки, в которой вы находитесь
    4. Создать внутри этой папки каталог с именем test1
    5. Перейти в папку test1
    6. Создать файл 1,2 и 3 внутри каталога test1
    7. Проверить содержимое каталога test1
    8. Перейти в домашнюю директорию
    9. Создать папку test2 внутри домашней директории
    10. Удалить папку test2
    11. Удалить файл 2 из папки test1
    12. Создать папку в домашней директории test3 и добавить в нее два файла
    13. Удалить папку test3
    14. Создать папку test4 в домашней директории
    15. Переместить файлы 1 и 3 из папки test1 в папку test4
    16. Добавить в файл 1 три строки со словами line
    17. Посмотреть содержимое файла 1
    18. Добавьте в файл 3 три строки со словами line
    19. Просмотрите содержимое двух файлов (1 и 3) сразу
    20. Используя один из редакторов замените все строки в файле 1

Решение задачи 1:
    1. touch  bash1.txt
    2. cd <адрес домашней директории>
    3. pwd
    4. mkdir test1
    5. cd test1
    6. touch 1.txt 2.txt 3.txt
    7. ls
    8. cd ..
    9. mkdir test2
    10. rmdir test2
    11. rm test1/2.txt
    12. mkdir test3
touch test3/1.txt test3/2.txt test3/3.txt
    13. rm -r test3
    14. mkdir test4
    15. mv test1/1.txt test4
mv test1/3.txt test4
    16. echo “line” >  test4/1.txt
echo “line” >>  test4/1.txt
echo “line” >>  test4/1.txt
    17. cat test4/1.txt
    18. echo “line” >  test4/3.txt
echo “line” >>  test4/3.txt
echo “line” >>  test4/3.txt
    19. cat test4/1.txt test4/3.txt
    20. nano  test4/1.txt
        1. нажимаем команду для поиска и замены строк ^\,  
        2. ищем строки с line, 
        3. заменяем на newline, 
        4. потверждаем замену Y,
        5. нажимаем команду на выход из редактора ^X, 
        6. подтверждаем изменения Y, 
        7. жмём кнопку Enter на клавиатуре.

Задача 2
    1. Предварительно создайте файл bash2.txt, в который вы будете добавлять выполненные команды.
    2. Зайти в домашнюю директорию через терминал.
    3. Создать папку test 3
    4. Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4
    5. Найдите строку row2 в файле 5
    6. Найдите строку row в папке test3
    7. Посчитайте сколько строк с содержимым row в файле 6
    8. Найдите файл 5 внутри папки test3
    9. Используя команду find, удалите файл 5
    10. Используя команду echo, добавьте слово test в файл 4
    11. Замените слово test в файле 4 на fail
    12. Добавьте в файл 4 слово test так, чтобы сохранилось содержимое
    13. Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе
    14. Убейте процесс 666 в консоли
    15. Узнайте доступность ресурса rusau.net, используя ping
    16. Отправьте 5 пакетов на сайт rusau.net
    17. Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/
    18. Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/


Решение задачи 2:
    1. touch  bash2.txt
    2. cd <адрес домашней директории>
    3. mkdir test3
    4. touch test3/4.txt test3/5.txt test3/6.txt
echo -e "row1\nrow2\nrow3\nrow4"| tee test3/4.txt test3/5.txt test3/6.txt
    5. grep "row2" test3/5.txt
    6. cd test3
grep "row" *.txt
    7. grep -c "row" 6.txt
    8. find -name "5.txt"
    9. find -name "5.txt" -exec rm {} \;
    10. echo "test" >> 4.txt
    11. nano 4.txt
        1. нажимаем команду для поиска и замены строк ^\,  
        2. ищем строкe с test, 
        3. заменяем на fail, 
        4. потверждаем замену Y,
        5. нажимаем команду на выход из редактора ^X, 
        6. подтверждаем изменения Y, 
        7. жмём кнопку Enter на клавиатуре.
    12. echo "test" >> 4.txt
    13. ps aux
    14. kill 666
    15. ping rusau.net
    16. ping -c 5 rusau.net
    17. curl https://petstore.swagger.io/v2/pet/findByStatus?status=available
    18. curl -H "Content-Type: application/json" -d '{"id": 7854,"username": "test345", "firstName": "Kevin", "lastName": "Sorbo", "email": "sorbo@example.com", "password": "iamthebest111", "phone": "45678934"}' https://petstore.swagger.io/v2/user
