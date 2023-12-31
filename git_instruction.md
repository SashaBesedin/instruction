![logo](17c86d4f862234bbc3a2f0a432a9f850.jpeg)
# **Работа с Git и GitHub**
# 1. Проверка установленного Git
В терминале выполнить команду `git version`. Если Git установлен появиться сообщение с информацией о версии программы, иначе будет сообщение об ошибке
# 2. Установка Git
Загружаем последнюю версию Git с сайта
https://git-scm.com/downloads.
Устанавливаем с настройками по умолчонию
# 3. Настройка Git
При первой использовании Git нужно представиться. Для этого нужно выполнить в терминале две команды:
```
git config --global user.email "sasch.besedin2017@yandex.ru
git config --global user.name "Aleksandr Besedin"
```
# 4. Инициализация репозитория

Для инициализации репозитория нужно выполнить в терминале команду `git init`.

# 5. Запись изменений в рипозитории

Для записи измененений файла в репозитории, нужно использовать команду `git add` и указанием файлов. Например, `git add filename.txt` или `git add .` (добавление всех измененных файлов).
Потом необходимо создать коммит, используя команду "git commit" и написав сообщение к коммиту. Например, `git commit -m "Добавить новую функцию"`.


# 6. Просмотр истории коммитов

Для просмотра истории изменений коммитов, нужно выполнить в терменале команду `git log`. 


# 7. Перемещение между сохранениями

Чтобы переместиться между коммитами необходимо выпонить в терминале команду `git checkout` и первые 4 символа из номера коммита.

# 8. Игнорирование файлов
Для того чтобы исключить из отслеживания в репозитории определеннве файлы или папки необходимо создать там файл ***.gitignore*** и записать в него названия или шаблоны, соответствующие таким файлам или папкам.

# 9. Создание веток а Git
Список веток в репозитории можно посмотреть с помощью команды:
```
git branch
```
Создать ветку можно командай:
```
git branch <название новой ветки>
```
По умолчанию имя сновной ветки в Git - `main`.

Для переключения между ветками используеться команда:
```
git checkout <название ветки>
```
# 10. Слияние веток и разрешение конфликтов
Для слияния выбранный ветке с текущей необходимо выполнить команду:
```
git merge <название выбранной ветки>
```
В случае если возникает конфликт, чтобы решить его необходимо выбрать нужный вариант из конфликтующих версий.
После разрешения конфликта необходимо снова закоммитить файл.

# 11. Удаление веток
Чтобы удалить ветку необходимо выполнить команду:
```
git branch -d <название ветки>
```
Ветку нельзя удалить если находишься в ней.

# 12. Работа с удалёнными репозиториями
При работе с кодом команде нужно иметь доступ к репозиторию с разных компьютеров для этого используются работу удалённую историями.

## 1. Создать аккаунт на GitHub
Чтобы начать работу с длинную историю необходимо для начало зарегистрировать свой аккаунт на гитхабе.
## 2. Создать локальный репозиторий
Для работы с удалённым репетиторе необходимо сначала создать локальный репозиторий с помощью команды:
```
git init
```
## 3. Создать удалённый репозиторий
После регистрации необходимо создать локальную историю нажав на плюсик в правом верхнем углу и выбрав название для репозитория.
## 4. Связать удалённый репозиторий с локальным
После создания удалённую историю GitHub предложит несколько вариантов наборов команд необходимых чтобы связать удалённый репозиторий с локальным. А так по молчанию лучше всего использовать команды:
```
git remote add origin https://github.com/SashaBesedin/instruction.git
```
```
git branch -M main
```
```
git push -u origin main
```
Первая команда связывает удалённый репозиторий с локальным. Вторая команда присваивает основной ветке название Main. 
Третья команда позволяет отправить локальный репозиторий на сервер