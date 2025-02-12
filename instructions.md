 # Создание проекта (репозитория = repository)

1. На странице github создайте новый репозиторий и скопируйте ссылку на него, кликнув на кнопку `Clone or download`. Ссылка выглядит следующим образом:

```
https://github.com/ilyavf/tx-builder.git
```

2. Откройте терминал и склонируйте репозиторий следующим образом:
```cmd
$ cd ~/dev
```
```
$ git clone https://github.com/ilyavf/tx-builder.git
```
```
$ cd tx-builder
```

Команда создаст новую папку (если такой нет в текущей директории) по имени проекта, в данном примере `tx-builder`.

3. Откройте проект в вашем любимом IDE.

# Работа с проектом

## Просмотр текущих изменений в терминале

Перейдите в папку с вашим проектом, например:
```
cd ~/dev/tx-builder
```

1. Список измененных файлов:
```
$ git status
```

2. Просмотр текущих изменений:
```
$ git diff
```

## Сохранение текущих изменений

1. Сохранение в локальном репозитории:
```
$ git commit -am "I made some changes. Put meaningful comment describing your changes"
```

2. Отгрузка на удаленный репозиторий (github):
```
$ git push

```

Флаги можно комбинировать, например:
```
$ git log -1 --name-status f64b35
```
```
$ git log -5 -p
```
Инициализация git-репозитория:
```
git init
```


- работает одинаково из любой директории, добавляет всю рабочую область

```
git add 
```
# путь относительно корневой директории
```
git add :/path/to/files/
```
# работает только в текущей директории
```
cd test
```
```
git add .
```
- эквивалентно этому:
```
git add :/test
```
# путь относительно текущей директории
```
cd test
```
```
git add ./path
```
- эквивалентно этому:
```
git add :/test/path
 ```
 -  Создадим файл, куда будем заносить файлы, которые не требуется отслеживать
 ```
touch .gitignore
```


- Слинкуем удалённый репозиторий как origin
```
git pull origin master
```
- Скачиваем последний правки с удалённого репозитория
```
git push --all
```

- список файлов с текущими изменениями
```
git status
```
- просмотр всез текущих изменений
```
git diff
```
 - просмотр изменений конкретного файла
```
git diff my-file.html
```
 - добавление коментария
```
git commit -am "коментарий"
```
- отгрузка коммитов на удаленный репозиторий
```
git push
```
-  просмотр последних 5 коммитов
```
git log -5
```
-  просмотр изменений последнего коммита
```
git log -1 -p
```
- просмотр последних 5 коммитов с перечнем измененных файлов
```
git log -5 --name-status
```
- просмотр изменений коммита с id `f64b35d28eaed0c127d07de66708d3f33a44d3f7` (достаточно 1х 5-6 символов)
```
git log -1 -p f64b35
```
- встроенная помощь git со списком всех доступных git-команд. Выход из режима просмотра - клавиша `q`.
```
git help
```
-  помощь по отдельным командам, например: `git help status`
```
git help <command>
```
- список файлов с текущими изменениями
```
git status
```

# копирование удаленного репозитория на локальный диск (в текущей директории будет создана папка по названию проекта

```
git clone <link to you repo>
```
- список файлов с текущими изменениями
```
git status
```
-  просмотр всез текущих изменений
```
git diff
```
- просмотр изменений конкретного файла
```
git diff my-file.html
```


# Шпаргалка по основным командам:

- Команда git add добавляет содержимое рабочей директории в индекс (staging area) для последующего коммита. По умолчанию git commit использует лишь этот индекс, так что вы можете использовать git add для сборки слепка вашего следующего коммита.
```
git add
```
- Команда git status показывает состояния файлов в рабочей директории и индексе: какие файлы изменены, но не добавлены в индекс; какие ожидают коммита в индексе. Вдобавок к этому выводятся подсказки о том, как изменить состояние файлов.
```
git status
```
- Команда git diff используется для вычисления разницы между любыми двумя Git деревьями. Это может быть разница между вашей рабочей директорией и индексом (собственно git diff), разница между индексом и последним коммитом (git diff --staged), или между любыми двумя коммитами (git diff master branchB).
```
git diff
```
- Команда git difftool просто запускает внешнюю утилиту сравнения для показа различий в двух деревьях, на случай если вы хотите использовать что-либо отличное от встроенного просмотрщика git diff.
```
git difftool
```
- Команда git commit берёт все данные, добавленные в индекс с помощью git add, и сохраняет их слепок во внутренней базе данных, а затем сдвигает указатель текущей ветки на этот слепок.
```
git commit
```
- Команда git reset, как можно догадаться из названия, используется в основном для отмены изменений. Она изменяет указатель HEAD и, опционально, состояние индекса. Также эта команда может изменить файлы в рабочей директории при использовании параметра --hard, что может привести к потере наработок при неправильном использовании, так что убедитесь в серьёзности своих намерений прежде чем использовать его.
```
git reset
```
- Команда git rm используется в Git для удаления файлов из индекса и рабочей директории. Она похожа на git add с тем лишь исключением, что она удаляет, а не добавляет файлы для следующего коммита.
```
git rm
```
- Команда git mv — это всего лишь удобный способ переместить файл, а затем выполнить git addдля нового файла и git rm для старого.
```
git mv
```
- Команда git clean используется для удаления мусора из рабочей директории. Это могут быть результаты сборки проекта или файлы конфликтов слияний.
```
git clean
```


Шпаргалка по ветвлению и слиянию|:

- Команда git branch — это своего рода “менеджер веток”. Она умеет перечислять ваши ветки, создавать новые, удалять и переименовывать их.
```
git branch
```
- Команда git checkout используется для переключения веток и выгрузки их содержимого в рабочую директорию.
```
git checkout
```
- Команда git merge используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит.
```
git merge
```
- Команда git mergetool просто вызывает внешнюю программу слияний, в случае если у вас возникли проблемы слияния.
```
git mergetool
```
- Команда git log используется для просмотра истории коммитов, начиная с самого свежего и уходя к истокам проекта. По умолчанию, она показывает лишь историю текущей ветки, но может быть настроена на вывод истории других, даже нескольких сразу, веток. Также её можно использовать для просмотра различий между ветками на уровне коммитов.
```
git log
```
- Команда git stash используется для временного сохранения всех незакоммиченных изменений для очистки рабочей директории без необходимости коммитить незавершённую работу в новую ветку.
```
git stash
```

- Команда git tag используется для задания постоянной метки на какой-либо момент в истории проекта. Обычно она используется для релизов.
```
git tag
```


