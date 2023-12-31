# Моё руководство по работе с Git
## 1. Начало работы. Подготовка рабочего пространства.
1. Первое, что делаем - создаём папку, в которой будем работать (хранить файл и его вариации). Имя папки желательно латиницей;
2. Второе - открываем её через *File-Open Folder*;
3. Открываем *Terminal-New Terminal*;
4. **git init** - в открытом терминале инициализируем эту папку (репозиторий) командой этой командой.
Н-р:  PS D:\Study\GeekBrains\My\Semester1\GeekGit\GitLecture> git init;
5. Создаём в папке-репозитории новый файл *File-New File*, даём ему имя и обязательно указывае расширение;
6. **git add *'название файла'*** - добавляем файл к отслеживанию гитом командой **git add**. Н-р:  
git add .\Lecture2.md
## 2. Сохранение версий документа.
1. Работаем с файлом - вносим нужные нам изменения;
2. На этапе, где могут появится разные варианыт нашей работы сохраняем файл с помощью комбинации клавиш *ctrl+S*, создаём точку сохранения - commit (англ. доверить) командой **git commit -m "*имя сохранения*"**
* **!!!** Каждое сохранение (commit) создаётся через: ctri+S - git add *имя файла* - git commit -m "*имя сохранения*"
3. **git diff** - с помощью этой команды  можем сравнить, какая разница между тем документом, в котором работаем сейчас и последним сохранением через commit;
4. **git log** - с помощью команды git log (это журнал) можно посмотреть историю всех сохраниний-commit;
5. У каждого commit (сохранения) есть номер. Н-р: commit a04347057eafd81e158862132aec9006351a6ff2 (HEAD -> master).  Используя первые несколько цифр номера commit можно переключаться между сохранениями, используя комманду checkout номер коммита.
А также перемещаться между ветками (branch) checkout branch_name;
## 3. Создание веток. Перемещение по веткам. Слияние веток.
1. **git branch *название ветки*** - команда для создания новой ветки;
2. Чтобы проверить, есть ли изменения не сохранёные использовать команду **git status**;
3. **git checkout *branch_name*** - переключение между ветками;
4. Чтобы посмотреть на какой ветке находимся используем команду **git branch**;
5. Чтобы объединить ветви командой **git merge**. Слияние необходимо делать из той ветки, в которую нужно внести новую. Н-р: из ветки master набираем команду **git merge *название ветки***;
6. При слиянии веток может возникнуть конфликт если в одинаковых строках в версиях разные данные. В этом случае git предложит нам самостоятельно решить, какую версию сохранить;
7. Добавление папки ИГНОР: создаем файл .gitignor и в этом файле укажим имя файла + расширение, который необходимо игнорировать, потом добаляем-коммитим его, название файла должено стать серого цвета;
8. Команда **git log --graph** позволяет посмотреть дерево коммитов;
## 4. Работа с изображениями.
9. Чтобы в MarkDown вставить изображение нужно написать: ![*текст описывающий изображение*](*имя файла*).
Пример: ![bears here](Bear.jpg);
7. Добавление папки ИГНОР: создаем файл .gitignor и в этом файле укажим имя файла + расширение, который необходимо игнорировать, потом добаляем-коммитим его, название файла должено стать серого цвета;
## 5. Дерево коммитов.
10. Команда **git log --graph** позволяет посмотреть дерево коммитов;
