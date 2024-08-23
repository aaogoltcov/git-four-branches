![git-logo](git-logo.png)

### [User Manual](https://git-scm.com/docs/user-manual)

# Введение

## Что такое GIT?
Git — это быстрая распределенная система контроля версий.

## Как получить Git-репозиторий
Лучший способ получить его — использовать команду `git-clone` для загрузки копии существующего репозитория.

Команда `clone` создает новый каталог с именем проекта. После того как вы перейдете в этот каталог, вы увидите, что он содержит копию файлов проекта, называемую рабочим деревом, вместе со специальным каталогом верхнего уровня с именем `.git`, который содержит всю информацию об истории проекта.
Несколько примеров для клонирования:

```
# Git itself:
$ git clone git://git.kernel.org/pub/scm/git/git.git

# the Linux kernel:
$ git clone git://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git
```

## Манипулирование ветвями
Создание, удаление и изменение ветвей выполняется быстро и легко - краткий обзор команд:

Перечислить все ветки.
```git
git branch
```

Создать новую ветку с именем `<branch>`, ссылающуюся на ту же точку в истории, что и текущая ветка.
```git
git branch <branch>
```

Создать новую ветку с именем `<branch>`, ссылающуюся на `<start-point>`, которую можно указать любым удобным для вас способом, в том числе с использованием имени ветви или имени тега.
```git
git branch <branch> <start-point>
```

Удалить ветку `<branch>`, если ветка не полностью объединена с вышестоящей веткой или не содержится в текущей ветке, эта команда завершится ошибкой с предупреждением.
```git
git branch -d <branch>
```

Удалить ветку `<branch>` независимо от ее объединенного статуса.
```git
git branch -D <branch>
```

Создать текущую ветку `<branch>`, обновив рабочий каталог так, чтобы он отражал версию, на которую ссылается `<branch>`.
```git
git switch <branch>
```

Создать новую ветку , `<new>` ссылающуюся на `<start-point>`, и проверьте ее.
```git
git switch -c <new> <start-point>
```

## Создание тегов

Git позволяет создать тег для ссылки на конкретный коммит.
```
git tag stable-1 1b2e1d63ff
```
