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
