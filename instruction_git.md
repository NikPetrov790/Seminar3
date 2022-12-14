#  **Инструкция для работы с Git**


## Что такое Git

Git - одна из реализаций распределенных систем контроля версий

![Логотип](git.jpg)

## Подготовка репозитория
Чтобы создать (инициализировать) новый репозиторий в текущей папке нужно внести в терминале команду:

    git init



## Создание коммитов
Чтобы создать новый коммит, нужно выполнить команду:

    git commit

Так же нужно описать суть внесенных изменений, для этого используем:

    git commit -m
Так же существует префикс, который позволяет добавить(изменить) и описать суть внесенных изменений в 1 строчку:

    git commit -a

### Добавление версионности
Чтобы вернуться в состояние "master" после выполненных операций(т.к в дальнейшнем,если не выполнить эту команду, могут возникнуть ошибки) нужно выполнить команду:

    git checkout master

Для добавление файлов или текста в самом файле, используется команда :

    git add


   
### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние или изменение репозитория, выполняется следующая команда:

    git status
Для просмотра истории коммитов выполняется команда:

    git log

Эта команда имеет большое количество опций поиска коммитов. Например, для того, чтобы упростить поиск всех коммитов, используется команда, которая показывает все коммиты:

    git log --oneline --all


### Фиксация изменений
Чтобы узнать все неподтвержденные изменения, внесенные после последнего коммита или сравнить файлы двух коммитов, используется команда:

    git diff

## Ветвление 

Ветки в git используются для разработки одной части функционала изолированно от других. Ветки позволяют **одновременно** работать над разными версиями проекта.

### Просмотр существующих веток

Для просмотра списка всех существующих веток нужно ввести команду:

    git branch

### Создание новых веток

Для создания новой ветки нужно ввести команду: 

    git branch <имя ветки>

Существует команда, котора позволяет не только создать ветку, но и одновременно переключиться на нее:

    git checkout -b <имя ветки>

### Слияние веток 

Для того, чтобы влить другую ветку в текущую нужно:
- переключиться на ту ветку **куда** вливаем
- ввести команду слияния, указав ту ветку, **которую** вливаем

Команда для слияния:

    git merge <имя ветки>

### Удаление веток

Чтобы удалить ветку нужно написать команду:

    git branch -d <имя ветки>

Существует еще один способ удаления ветки (не рекомендуется к использованию, т.к. пропадет вся информация, которая находилась в ветке). Для того, чтобы им воспользоваться нужно ввести команду:

    git branch -D <имя ветки>

### Создание нового удаленного репозитория
Для того, чтобы посмотреть список удаленных репозиториев нужно написать команду:

    git remote

Также можно указать ключ <-v>, чтобы посмотреть адреса и записи, привязанные к репозиторию:
 
    git remote -v

### Отправка изменений в удаленный репозиторий

Чтобы отправить вашу ветку **master** на сервер **origin** нужно выполнить команду, которая отправит ваши коммиты:

    gut push origin master
    
### Получение изменений
 
Чтобы автоматически получить получить изменения из удаленной ветки и слить их со своей текущей нужно написать команду:

    git pull

Команда **git clone**  автоматически настраивает вашу локальную ветку **master** на отслеживание удаленной ветки **master** на сервере,с которого вы клонировали репозиторий.

### Просмотр удаленного репозитория
Чтобы получить побольше информации об одном из удаленных репозиториев, мы можем использовать команду:

    git remote show <remote>
### Удаление и переименование удалённых репозиториев
Для переименования удаленного репозитория можно выполнить команду:

    git remote rename <remote> <new remote>
    
Если вы хотите удалить удаленный репозиторий, вы можете использовать команду:

    git remote rm <remote>
