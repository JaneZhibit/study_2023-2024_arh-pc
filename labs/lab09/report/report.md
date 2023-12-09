---
## Front matter
title: "Лабораторная работа №9"
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

Продолжение изучения языка ассемблера, использование подпрограмм и знакомство с  методами отладки при помощи GDB.



# Выполнение лабораторной работы

Для начала создадим каталог для 9 лабораторной работы, создадим файл и не забудем скопировать файл in_out.asm в этот же каталог(рис. @fig:001).

![Создание каталога и файла](image/1.png){#fig:001 width=70%}



Затем заполним файл текстом из Листинга 9.1, создадим исполняемый файл и запустим(рис. @fig:002).

![Запуск программы](image/2.png){#fig:002 width=70%}


Потом изменим программу, добавив подпрограмму _subcalcul и также запустим ее(рис. @fig:003).

![Создание подпрограммы](image/3.png){#fig:003 width=70%}



Далее добавим файл lab09-2.asm с текстом программы из Листинга 9.2, создадим исполняемый файл с ключом -g для отладочной информации и загрузим его в отладчик(рис. @fig:004).

![Загрузка в отладчик(и создание файла)](image/4.png){#fig:004 width=70%}



Затем командой run запустим программу(рис. @fig:005), также добавим брейкпоинт и еще раз запустим ее(рис. @fig:006).

![Запуск программы](image/5.png){#fig:005 width=70%}



![Установка брейкпоинта и запуск](image/6.png){#fig:006 width=70%}



Посмотрим дисассимилированный код программы командой disassemble(рис. @fig:007), также переключимся на отображение с Intel’овским синтаксисом(рис. @fig:008).
Отличаются порядком операндов, записью числовых констант, наличием/отсутствием % перед именем регистра и тд.


![Дисассимилированный код](image/7.png){#fig:007 width=70%}



![Дисассимилированный код с Intel’овским синтаксисом](image/8.png){#fig:008 width=70%}



Далее включим режим псевдографики и сразу посмотрим уже установленные ранее точки останова(рис. @fig:009)

![Режим псевдографики](image/9.png){#fig:009 width=70%}



Установим еще один брейкпоинт и еще раз проверим информацию о всех точках останова(рис. @fig:010).

![Установка и просмотр точек останова](image/10.png){#fig:010 width=70%}



Чтобы посмотреть содержимое регистров введем info registers(рис. @fig:011).

![info registers](image/11.png){#fig:011 width=70%}



Затем посмотрим значение переменной msg1 по имени и msg2 по адресу(рис. @fig:012).

![Просмотр значений переменных](image/12.png){#fig:012 width=70%}



После инструкцией set изменим символы в переменных msg1 и msg2(рис. @fig:014)

![Изменение символов в переменных](image/14.png){#fig:014 width=70%}



Наконец командой print посмотрим значения регистра(в 16ричном,2оичном и символьном форматах)(рис. @fig:015) и изменим значение регистра ebx(симол и число)(рис. @fig:016).

![Просмотр значения edx](image/15.png){#fig:015 width=70%}



![Изменение регистра еbx](image/16.png){#fig:016 width=70%}



Следующим этапом скопируем файл из предыдущией работы и создадим исполняемый файл(рис. @fig:017).

![Копирование файла](image/17.png){#fig:017 width=70%}



Загрузим эту программу в отладчик использовав ключ --args, установим точку останова и запустим ее(рис. @fig:018).

![Запуск прораммы в отладчике](image/18.png){#fig:018 width=70%}



В конце посмотрим, что число аргументов равно 5 - посмотрим остальные позиции стека по адресу(рис. @fig:019).

![Просмотр позиций стека](image/19.png){#fig:019 width=70%}



# Задание для самостоятельной работы

1. Преобразуем программу из 8 лабораторной работы, реализовав вычисление функции как подпрограммы(рис. @fig:020).

![Код и запуск программы](image/20.png){#fig:020 width=70%}



2. Определение и исправление ошибки из Лиситнга 9.3
C  помощью отладчика gdb, поочередно выполняя команды и следя за значениями регистров, видим, что ошибка возникает из-за неправильной записи резултата сложения в регистр ebx, а не eax, так как при последующем умножении, умножается именно регистр eax(рис. @fig:021).

![Поиск ошибки](image/21.png){#fig:021 width=70%}


Исправим код программы и запустим ее(рис. @fig:022).


![Код и запуск программы](image/22.png){#fig:022 width=70%}



# Выводы

В ходе работы было произведено знакомство с методами и возможностями отладки программ, применены подпрограммы.


