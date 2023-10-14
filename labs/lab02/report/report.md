---
## Front matter
title: "Отчет по лабораторной работе №2"
subtitle: "Дисциплина: Архитектура компьютера"
author: "Жибицкая Евгения Дмитриевна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"


## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Цель работы

Познакомиться с системой контроля версий git, изучить ее идеологию и применение,  приобрести практические навыки при работе с данной системой.


# Выполнение лабораторной работы

Для начала создадим учетную запись на сайте http://github.com/ (рис. @fig:001).

![Создание учетной записи.](image/1.png){#fig:001 width=70%}


После сделаем предварительную конфигурацию git.  Для этого необходимо в терминале ввести команду git config --global и user.name/email (рис. @fig:002).

![Создание предварительной конфигурации git.](image/2.png){#fig:002 width=70%}


Также настроим utf-8 (core.quotepath false)(рис. @fig:003), назовем начальную ветку master, настроим параметры autocrlf  и safecrlf (рис. @fig:004).

![Настройка utf-8.](image/3.png){#fig:003 width=70%}

![Настрока параметров autocrlf, safecrlf, присвоение имени master ветке.](image/4.png){#fig:004 width=70%}


Затем необходимо создать SSH ключ(для индетификации пользователя на сервере)(рис. @fig:005),(рис. @fig:006),(рис. @fig:007).

![Создание ключа.](image/5.png){#fig:005 width=70%}

![Считывание и копирование ключа.](image/6.png){#fig:006 width=70%}

![Загрузка ключа.](image/7.png){#fig:007 width=70%}


Создадим каталог для предмета  Архитектура компьютера, имеющий следуюущий путь: ~/work/study/2023-2024/»Архитектура компьютера», используем для этого команду mkdir и ключ p (рис. @fig:008).

![Загрузка ключа.](image/8.png){#fig:008 width=70%}


Также надо создать репозиторий на основе шаблона, это можно сделать через сайт. Переходим на страницу с шаблоном курса, используем шаблон, задаем имя  репозитория (рис. @fig:009).

![Создание репозитория. ](image/9.png){#fig:009 width=70%}


После открываем терминал, переходим в каталог курса (рис. @fig:010)и клонируем созданный репозиторий (рис. @fig:011).

![Переход в каталог курса. ](image/10.png){#fig:010 width=70%}

![Клонирование каталога. ](image/11.png){#fig:011 width=70%}


Последнее, что необходимо сделать, это настроить каталог.
Для начала перейдем в каталог(рис. @fig:012) , удалим лишние файлы(рис. @fig:013), потом создадим необходимые каталги(course)(рис. @fig:014) и отправим файлы на сервер(рис. @fig:015),(рис. @fig:016),(рис. @fig:017).

![Переход в каталог. ](image/12.png){#fig:012 width=70%}

![ Удаление лишних файлов.  ](image/13.png){#fig:013 width=70%}

![Создание каталога COURSE. ](image/14.png){#fig:014 width=70%}

![Добавление всех созданных файлов и каталогов. ](image/15.png){#fig:015 width=70%}

![Сохранение всех изменений. ](image/16.png){#fig:016 width=70%}

![Отправка изменений в удаленный репозиторий. ](image/17.png){#fig:017 width=70%}


Убедимся, в правильности созданной иерархиии в локальном репозитории (рис. @fig:018) и  на github (рис. @fig:019).

![Проверка на наличие каталога в локальном репозитории. ](image/18.png){#fig:018 width=70%}

![Проверка на наличие каталога во внешнем репозитории. ](image/19.png){#fig:019 width=70%}



# Задание для самостоятельной работы

Задание 1. Создайте отчет по выполнению работы  в соответствующем каталоге рабочего пространства.

Для выполнения задания используем команду mv и переместим файл в нужные каталоги(подкатологи) (рис. @fig:020).

![Перемещение файла с отчетом. ](image/20.png){#fig:020 width=70%}


Задание 2.  Скопируйте отчеты по выполнению предыдущих работ в соответствующие каталоги рабочего пространства.

Используя команду копирования, скопируем 1й отчет в нужный каталог  и убедимся, что все правильно (рис. @fig:021, (рис. @fig:022).

![Копирование отчета. ](image/21.png){#fig:021 width=70%}

![Проверка на корректность выполнения команды. ](image/22.png){#fig:022 width=70%}


Задание 3.  Загрузка файлов на github.

Чтобы загрузить файлы на github, перейдем в нужные каталоги, затем используем команды git add(добавление всех файлов), git commit(сохрание файлов и комментарий), git push(отправка изменений в центральный репозиторий) (рис. @fig:023), (рис. @fig:024).

![Использование команд  git add, git commit. ](image/23.png){#fig:023 width=70%}

![Использование команды  git push. ](image/24.png){#fig:024 width=70%}


Проверим, что все загрузилось (рис. @fig:025).

![Проверка выполнения. ](image/25.png){#fig:025 width=70%}


# Выводы

В ходе выполнения работы  мы ознакомились с системой  git, создали акккаунт на github, SSH ключ, приобрели различые навыки при работе с системой контроля версий.


:::
