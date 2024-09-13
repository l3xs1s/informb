---
## Front matter
title: "Индивидуальный проект. Отчёт о выполнении №1


Информационная безопасность"
subtitle: " Установка и конфигурация
операционной системы на виртуальную машину"
author: "Выполнил: Негматуллаев Бежан, 


НФИбд-02-21, 1032217048"



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
mainfont: Times New Roman
romanfont: Times New Roman
sansfont: Times New Roman
monofont: Times New Roman
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

Целью первого этапа проекта является установка дистрибутива Kali Linux на вирутальную машину.

# Конфигурация виртуальной машины

Первым делом требуется предварительо загрузить сам дистрибутив с официального сайта, после загрузки дистрибутива, открываем приложение VirtualBox, 
а затем создаем и конфигурируем нвоую виртуальную машину (раздел Машина -> Создать). Даем название виртуальной машине, выбираем тип дистрибутива RedHat.

![Окно создания новой машины](Screens/1.PNG){ #fig:001 width=60% height=60% }

Указываем размер оперативной памяти.

# Конфигурация установки ОС

Запускаем виртуальную машину, выбираем Graphical install.

![Установка](Screens/2.PNG){ #fig:005 width=60% height=60% }

Выбираем язык - Русский.

![Выбор языка системы](Screens/3.PNG){ #fig:006 width=60% height=60% }

Выбираем имя хоста

![Выбор имени хоста](Screens/4.PNG){ #fig:007 width=60% height=60% }

Выбор основного имени пользователя, имени пользователя и пароля

![Выбор основного имени пользователя](Screens/5.PNG){ #fig:009 width=60% height=60% }

![Пароль](Screens/6.PNG){ #fig:011 width=60% height=60% }

Продолжаем установку

Далее появляется выбрать дополнительное програмное обеспечение для установки, оставляем все как есть и продолжаем установку

![Выбор дополнительного ПО](Screens/7.PNG){ #fig:016 width=60% height=60% }

# Заключение

Был установлен дистрибутив Kali Linux на виртуальную машину.