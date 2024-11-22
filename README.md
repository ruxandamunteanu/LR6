# LR6
Лабораторная работа №6

# Цель работы 
Изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием. 

# Порядок выполнения работы 

### Настройка и подготовка к работе с GitHub
Был сделан форк, уставновлен Git и изменено имя пользователя и email с помощью команд: 
```bash
$ git config --global user.name " 4319 Мунтяну Р."
```

```bash
$ git config --global user.email "ruxandam2005@gmail.com"
```
![Рисунок 1](https://github.com/ruxandamunteanu/LR6/blob/report/images/1.png?raw=true)

### Клонирование репозитория 
Следующим шагом в папке LR был клонирован личный удалённый репозиторий на компьютер:
```bash
$ git clone 
```
![Рисунок 2](https://github.com/ruxandamunteanu/LR6/blob/report/images/2.png?raw=true)

### Добавление файла через интерфейс GitHub
C помощью Add file << Create new file  был создан файл new_file и подтянуты изменения в локальный репозиторий.

![Рисунок 3](https://github.com/ruxandamunteanu/LR6/blob/report/images/3.png?raw=true)

### Просмотр истории и последних изменений веток
История операций для каждой из веток:
![Рисунок 4](https://github.com/ruxandamunteanu/LR6/blob/report/images/4.png?raw=true)

Последние изменения:
![Рисунок 5](https://github.com/ruxandamunteanu/LR6/blob/report/images/5.png?raw=true)

### Cлияние в ветку master, разрешение конфликта и удаление побочной ветки 
В ветке master было выполнено слияние c веткой branch1, в результате чего получено сообщение о конфликте:
![Рисунок 6](https://github.com/ruxandamunteanu/LR6/blob/report/images/6.png?raw=true)

Разрешение конфликта:

![Рисунок 7](https://github.com/ruxandamunteanu/LR6/blob/report/images/7.png?raw=true)

Завершение слияния:
![Рисунок 8](https://github.com/ruxandamunteanu/LR6/blob/report/images/8.png?raw=true)

Удаление побочной ветки:

![Рисунок 9](https://github.com/ruxandamunteanu/LR6/blob/report/images/9.png?raw=true)

### Внесение изменений с комментариями и откат коммита
Изменение текста в файле new_file  и создание коммита:
![Рисунок 10](https://github.com/ruxandamunteanu/LR6/blob/report/images/10.png?raw=true)

Создание нового файла info.txt с текстом, просмотр его содержимого и создание коммита:
![Рисунок 11](https://github.com/ruxandamunteanu/LR6/blob/report/images/11.png?raw=true)

Изменение содержимого info.txt и его коммит:
![Рисунок 12](https://github.com/ruxandamunteanu/LR6/blob/report/images/12.png?raw=true)

Произведен откат коммита:
![Рисунок 13](https://github.com/ruxandamunteanu/LR6/blob/report/images/13.png?raw=true)

### Создание ветки для отчёта
Была создана ветка report с помощью команды:
```bash
 $ git checkout -b report 
```
![Рисунок 14](https://github.com/ruxandamunteanu/LR6/blob/report/images/14.png?raw=true)

### Лог команд 
```bash
# установка глобального имени пользователя 
$ git config --global user.name " 4319 Мунтяну Р."
# установка глобального email
$ git config --global user.email "ruxandam2005@gmail.com"
# создание копии удаленного репозитория
$ git clone 
# получение изменений из удаленного репозитория и их слияние с текущей веткой
$ git pull
# получение истории коммитов текущей ветки
$ git log 
# отображение всей истории коммитов с графическим представлением веток и метками
$ git log --all --graph --oneline --decorate
# слияние ветки branch1 с текущей веткой 
$ git merge branch1
# добавление файла mergefile.txt в индекс
$ git add mergefile.txt
# просмотр текущего состояния репозитория
$ git status 
# создание коммита о разрешении конфликта
$ git commit -m "Разрешен конфликт при слиянии в ветку master"
# удаление побочной ветки branch1
$ git branch -d branch1
# добавление файла new_file в индекс
$ git add new_file
# создание коммита о изменении new_file
$ git commit -m "Изменение текста в new_file"
# создание файла info.txt с содержанием
$ echo "Это новый файл с информацией" > info.txt
# вывод содержимого файла info.txt в терминал.
$ cat info.txt
# добавление файла info.txt в индекс
$ git add info.txt
# создание коммита о создании info.txt
$ git commit -m "Создан файл info с информацией"
# добавление файла info.txt в индекс
$ git add info.txt
# создание коммита о изменении info.txt
$ git commit -m "Содержимое файла info изменено"
# откат последнего коммита 
$ git reset HEAD~1
# создание и переключение на новую ветку report
$ git checkout -b report
# пуш ветки report на удаленный репозиторий и ее соединение с удаленной веткой 
$ git push --set-upstream origin report
```
### История операций
```bash
$ git log --pretty=format:"%h | %ad | %an | %s" --date=short
0457b1c | 2024-11-22 | 4319 Мунтяну Р. | Добавлена папка со скриншотами
0098377 | 2024-11-21 | 4319 Мунтяну Р. | Создан файл info с информацией
85963f1 | 2024-11-21 | 4319 Мунтяну Р. | Изменение текста в new_file
3b9ea40 | 2024-11-21 | 4319 Мунтяну Р. | Разрешен конфликт при слиянии в ветку master
fc197f9 | 2024-11-21 | ruxandamunteanu | Добавлен new_file через интерфейс
921f53b | 2020-11-21 | Kurtyanik | Обновление информации
0f9f50d | 2020-11-21 | Kurtyanik | Заполнил файл
c08a654 | 2020-11-21 | Kurtyanik | Файл создан пустым
3c6e913 | 2020-11-21 | Kurtyanik | Initial commit
```
