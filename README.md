# Шпаргалка Git

## Настройка Git

Чтобы участникам проекта было понятно, кто и какие изменения вносил, нужно представиться
и указать имя пользователя и адрес электронной почты.
Сделать это можно с помощью команды `git config --global`.
При этом не имеет значения, в какой директории вы находитесь прямо сейчас, вызов этой команды сработает везде.

В качестве значения `user.name` нужно указать свое имя или никнейм.
Для настройки параметра `user.email` указывают электронную почту. Например:

`$ git config --global user.name "User Namovich"`
// имя или ник нужно написать латиницей и в кавычках

`$ git config --global user.email username@yandex.ru`
// здесь нужно указать свой настоящий email

Все глобальные настройки Git хранит в файле `.gitconfig`. Команда запишет в этот файл указанные имя и имейл.
Чтобы убедиться в этом, можно вызвать команду для чтения файлов `$ cat ~/.gitconfig`.
В ответ командная строка вернет текущие значения настроек.

## Инициализируем репозиторий

Чтобы Git начал отслеживать изменения в проекте, папку с файлами этого проекта нужно сделать Git-репозиторием.
Для этого следует переместиться в нее (папку вашего проекта) и ввести команду `git init`.

В подпапке `.git` Git будет хранить всю служебную информацию.

### Проверить состояние репозитория

После инициализации репозитория запустите команду `git status` - она показывает текущее состояние репозитория.

### Подготовить файлы к сохранению

Чтобы подготовить файлы к сохранению, запустите команду `git add --all`, Git начнет следить за добавленными или измененными файлами. Так же можно добавить текущую папку целиком командой `git add .`.

### Выполнить коммит

Сделать коммит можно командой `git commit` с ключом `-m`, который присваивает коммиту сообщение.
Обычно в таком сообщение поясняется, что именно было изменено.

### Хеш - идентификатор коммита

Git хранит таблицу соответствий `хеш -> информация о коммите`. Если вы знаете хеш, вы можете узнать все остальное: автора и дату коммита и содержимое закоммиченных файлов.
Обычно хеш - это короткая (40 символов) строка, которая состоит из цифр 0-9 и латинских букв A-F.

# Шпаргалка markdown

## Выделение текста

Вы можете выделять текст в markdown с помощью символов `_` или `*`. Например:

Пример _курсива_ и **жирного** текста.

## Заголовки

Заголовки можно создавать с помощью символа `#`. Чем больше `#`, тем меньше заголовок. Например:

# Заголовок первого уровня

## Заголовок второго уровня

### Заголовок третьего уровня

## Выделение кода

Чтобы выделить текст как код, поместите его в тройные кавычки `````.

```
mkdir my_project
cd my_project
git init
```

Это лишь некоторые функции markdown.

Шпаргалка по маркдауну [GitHub](https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c)
