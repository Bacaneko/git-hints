# git-hints

## Небольшой гит-репозиторий для самостоятельной работы

`git clone https://github.com/PraktikumJava/git-hints.git`

## Как читать git status

Статусы untracked/tracked, staged и modified

1) 'untracked' - новые файл, нет предыдущих версий, зафиксированных в коммитах или через команду 'git add'

2) 'modified' + 'git add' = 'staged' + 'tracked'

3) 'git commit' = 'tracked'

4) 'modified' - измененный файл

Команда 'git status' показывают только 3 состоянию файла:
'staged', 'modified', 'untracked'

## Как откатить измениня, если всё сломалось

1) git restore --staged hello.txt - переведи файл hello.txt из состояния staged обратно в untracked или modified;

2) git restore hello.txt - верни файл hello.txt к последней версии, которая была сохранена через git commit или git add

3) git reset --hard b576d89 - удали все незакоммиченные изменения из staging и «рабочей зоны» вплоть до указанного коммита

## Просмотреть изменения

1) git diff - покажи изменения в «рабочей зоне», то есть в modified-файлах

2) git diff a9928ab 11bada1 - выведи разницу между двумя коммитами

3) git diff --staged - покажи изменения, которые добавлены в staged-файлах

## Ветки

### Создание веток

1) git branch feature/the-finest-branch — создай ветку от текущей с названием feature/the-finest-branch

2) git checkout -b feature/the-finest-branch — создай ветку feature/the-finest-branch и сразу переключись на неё

### Навигация по веткам

1) git branch — покажи, какие есть ветки в репозитории и в какой из них я нахожусь

2) git branch -a — покажи все известные ветки, как локальные (в локальном репозитории), так и удалённые (в origin на GitHub)

3) git checkout feature/br — переключись на ветку feature/br

### Сравнение веток

1) git diff main HEAD — покажи разницу между веткой main и указателем на HEAD

2) git diff HEAD~2 HEAD — покажи разницу между тем коммитом, который был два коммита назад, и текущим

### Удаление веток

1) git branch -d br-name — удали ветку br-name, но только если она является частью main

2) git branch -D br-name — удали ветку br-name, даже если она не объединена с main

### Слияние веток

1) git merge main — объедини ветку main с текущей активной веткой
