# Git

установка
> apt-get install git

#### Настройка
> git config --global user.name "USERNAME"

> git config --global user.email "EMAIL"

> git config --global push.default simple

установка окончания строк
> git config --global core.autocrlf input

> git config --global core.safecrlf true

алиасы - alias
> vim ~/.gitconfig
```
[alias]
	hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
```

создать репозиторий из текущего каталога
> git init

#### Добавить файл в репозиторий
проиндексировать файл
> git add index.html

проиндексировать все файлы
> git add .

коммит
> git commit - m "comment commit"

коммит без комментария
> git commit

изменить предыдущий коммит
> git commit --amend -m "comment"

проверка состояния репозитория
> git status

возвращает рабочий каталог к предыдущему состоянию
> git checkout <hash>

к последней версии в ветке master
> git checkout master

переключение на предыдущую версию (v1 - тег)
> git checkout v1^

> git checkout v1~1

отмена изменений до индексации(git add )
> git checkout index.html

отмена индексации (git add )
> git reset HEAD index.html

отмена коммита по хэш
> git revert HEAD --no-edit # отмена последнего коммита

сброс коммитов до нужного
> git reset --hard v1

история проекта
> git log

> git hist --all

создание тегов для коммитов
> git tag v1

> git tag v1-beta

сброс ветки до коммита
> git reset --hard <hash>

переместить файл (проиндексированно и готово к коммиту)
> git mv index.html hello.html

создать клон репозитория
> git clone <rep> <clone_rep>

извлечь новые коммиты из удалённого репозитория
> git fetch

слить извлечённые изменения с локальной веткой
> git merge origin/master

извлечение и слияние изменений одной командой
> git pull



> git diff index.html

> git show HEAD

подключаем удалённые репозиторий, origin - локальное название
> git remote add origin https://github.com/talentin/test_rep.git

отправка локального репозитория ветка master
на удалённый репозиторий origin, -u - запомнить куда отпралять
> git push -u origin master

# SSH for Git
Generating a new SSH key
> ssh-keygen -t rsa -b 4096 -C "email"
Adding SSH key to the ssh-agent
> eval "$(ssh-agent -s)"

> ssh-add ~/.ssh/id_rsa

Adding SSH key to GitHub account
> Settings > SSH and GPG keys > Add SSH key > Title > Key from id_rsa.pub

> ssh -T git@github.com

Switch remote urls from HTTPS to SSH
> git remote set-url origin git@github.com:USERNAME/REPOSITORY.git


