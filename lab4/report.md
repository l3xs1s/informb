---
## Front matter
title: "Отчёт по лабораторной работе №4


Информационная безопасность"
subtitle: "Дискреционное
разграничение прав в Linux. Два пользователя"
author: "Выполнил: Негматуллаев Бежан Шухратович , 


НФИбд-02-21, 1032215469"

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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получение практических навыков работы в консоли с расширенными
атрибутами файлов.

# Выполнение лабораторной работы

## Атрибуты файлов

1. От имени пользователя guest определите расширенные атрибуты файла
Установите командой chmod 600 file1 на файл file1 права, разрешающие чтение и запись для владельца файла.

![(рис. 1.)](image/1.PNG){ #fig:002 width=70% height=70% }


2. Попробуйте установить на файл /home/guest/dir1/file1 расширенный атрибут a от имени пользователя guest:
chattr +a /home/guest/dir1/file1. В ответ вы должны получить отказ от выполнения операции.

![(рис. 2.)](image/2.PNG){ #fig:008 width=70% height=70% }

3. Зайдите на третью консоль с правами администратора либо повысьте
свои права с помощью команды su. Попробуйте установить расширенный атрибут a на файл /home/guest/dir1/file1 от имени суперпользователя:chattr +a /home/guest/dir1/file1

![(рис. 3.)](image/3.PNG){ #fig:010 width=70% height=70% }

4. От пользователя guest проверьте правильность установления атрибута:
lsattr /home/guest/dir1/file1

![(рис. 4.)](image/4.PNG){ #fig:013 width=70% height=70% }


5. Выполните дозапись в файл file1 слова «test» командой
echo "test" /home/guest/dir1/file1. После этого выполните чтение файла file1 командой
cat /home/guest/dir1/file1
Убедитесь, что слово test было успешно записано в file1

![(рис. 5.)](image/5.PNG){ #fig:014 width=70% height=70% }

6. Попробуйте удалить файл file1 либо стереть имеющуюся в нём информацию командой
echo "abcd" > /home/guest/dirl/file1
Попробуйте переименовать файл.

![(рис. 6.)](image/6.PNG){ #fig:015 width=70% height=70% }

7. Попробуйте с помощью команды chmod 000 file1
установить на файл file1 права, например, запрещающие чтение и запись для владельца файла. Удалось ли вам успешно выполнить указанные команды?

![(рис. 7.)](image/7.PNG){ #fig:015 width=70% height=70% }

Снимите расширенный атрибут a с файла /home/guest/dirl/file1 от
имени суперпользователя командой
chattr -a /home/guest/dir1/file1
Повторите операции, которые вам ранее не удавалось выполнить. Ваши
наблюдения занесите в отчёт.
 Повторите ваши действия по шагам, заменив атрибут «a» атрибутом «i».
Удалось ли вам дозаписать информацию в файл? Ваши наблюдения занесите в отчёт

![(рис. 8.)](image/8.PNG){ #fig:015 width=70% height=70% }

# Вывод

Были получены практические навыки работы в консоли с группами, закреплены теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux



