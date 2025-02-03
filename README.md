GIT - Полный Курс Git и GitHub Для Начинающих [4 ЧАСА]
https://www.youtube.com/watch?v=O00FTZDxD0o


https://git-scm.com/


21:20
git config --list
git config --global user.name "Bogdan Stashchuk"
git config --global user.email "bstashchuk@gmail.com"


24:45
cd ~/Desktop
mkdir my-project
cd my-project
echo "Some text" > file.txt // Создание файла с текстом
ls // Список файлов в папке
cat file.txt // Прочитать файл
rm file.txt // Удаление файла
pwd // Посмотреть где находимся


34:00
git init // создание нового Git репозитория
// создаётся скрытая папка .git
ls -la // Увидеть скрытые файлы и папки на Linux, Mac
ls -Force // тоже на PowerShell(Windows)


38:00
cd my-project
git init
git branch -m <name> // Переименовать ветку по умолчанию


55:00 ===== РАБОЧИЙ ПРОЦЕСС GIT
git add
git commit
git checkout


58:00 ===== СТАТУСЫ ОТСЛЕЖИВАНИЯ ФАЙЛОВ
untracked
staged
unmodified // Статус файла в закоммиченном репозитории
modified
staged


1:01:00 ТИПЫ ОБЪЕКТОВ В GIT
Blob (файл)
Tree (папка)
Commit (коммит)
Annotated Tag (аннотированный тег)


1:37:20 ОСНОВНЫЕ КОМАНДЫ
git status
git add <files>
git commit -m "<message>"
git log
git checkout <commit hash> // Увидеть изменения в текущей директории
git checkout <branch name>


2:00:30
// Посмотрим тип и содержимое двоичных файлов в папке ./git/objects/
git cat-file -t 7993858 // читать тип объекта GIT
git cat-file -p 7993858 // читать содержимое объекта

2:11:20 
// Уже создали два коммита
git log

2:21:43 ВЕТКИ В GIT


2:29:50
git branch new-branch
git checkout new-branch
git checkout -b <branch name> // создать и переключиться на ветку
	// (git switch -c <new-branch>)
git branch // Посмотреть сущесвующие ветки
git branch -m <new branch name> // Переименовать текущую ветку
git branch -d <branch name> // Удалить ветку


2:37:00 СЛИЯНИЕ ВЕТОК


2:44:14 Команда для слияния веток
git merge <feature branch name> // Слияние другой ветки в текущую ветку (receiving branch)


2:51:21
https://code.visualstudio.com/
Ctrl + Shift + P
>code
Shell Command: Install 'code' command in PATH
code . // Открыть VScode в текущей папке


3:10:00
// Получим изменения в текущую ветку main из ветки new-feature
git merge -m "Merging new-feature into main" new-feature
git cat-file -p c8a2aa2
git branch -d new-feature
git log --all --graph // Посмотреть все коммиты и построить граф
// В реальных проектах создают ветку stage, которая находится между production и development


3:17:30 СЕРВИСЫ ХОСТИНГА GIT РЕПОЗИТОРИЕВ
git clone <url>
origin // Имя remote репозитория по-умолчанию
git branch -a // Увидеть все ветки находящиеся на remote серверах
git checkout <branch name> // Переключиться на любую ветку
git fetch // Скачать
git pull // Скачать и объеденить(merge)
git push // Выгрузить



3:30:00 СВЯЗЬ С REMOTE РЕПОЗИТОРИЕМ GITHUB
https://github.com/
git remote add origin <url> // Создаём связь в remote сервером
git branch -M main
git push -u origin <branch> // Отправляем из текущей ветки в ветку <branch>


3:35:51 Практика по клонированию удалённого репозитория
https://github.com/bstashchuk
https://github.com/bstashchuk/docker
git remote -v
git branch -vv
git log --oneline --graph


3:46:22 Создание авторизационного токена на GitHub
Personal access tokens
https://github.com/settings/apps
https://github.com/settings/tokens
// на GitHub получаем секретный ключ, который нужно скопировать и сохранить 
// и использовать в качесве пароля

git reset
git revert
git hooks
git stash
git rebasing