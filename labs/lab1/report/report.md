---
## Front matter
title: "Лабораторная работа №1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
author: "Солдатов А. Е."

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Установить операционную систему на виртуальную машину и настроить минимальные необходимые сервисы.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

## Создание новой виртуальной машины

Указал имя виртуальной машины и тип операционной системы (рис. [-@fig:001]).

![Имя виртуальной машины](./image/1.png){#fig:001 width=70%}

Указал имя пользователя и пароль (рис. [-@fig:002]).

![Имя пользователя](./image/2.png){#fig:002 width=70%}

Указал размер памяти и количество ядер (рис. [-@fig:003]).

![Память и ядра](./image/3.png){#fig:003 width=70%}

Задал конфигурацию жесткого диска (рис. [-@fig:004]).

![Конфигурация жесткого диска](./image/4.png){#fig:004 width=70%}

Получилась такая конфигурация (рис. [-@fig:005]).

![Итоговая конфигурация](./image/5.png){#fig:005 width=70%}

## Установка ОС

Запустил виртуальную машину и указал английский язык (рис. [-@fig:006]).

![Выбор языка](image/6.png){#fig:006 width=70%}

Настроил переключение раскладки (рис. [-@fig:007]).

![Переключение раскладки](./image/7.png){#fig:007 width=70%}

Указал часовой пояс (рис. [-@fig:008]).

![Часовой пояс](./image/8.png){#fig:008 width=70%}

Выбрал базовое и дополнительное окружение (рис. [-@fig:009]).

![Окружение](./image/9.png){#fig:009 width=70%}

Отключил KDUMP (рис. [-@fig:0010]).

![Отключение KDUMP](./image/10.png){#fig:010 width=70%}

Место установки оставил без изменения (рис. [-@fig:011]).

![Место установки ОС](./image/11.png){#fig:011 width=70%}

В сетевом соединении указал новое имя узла (рис. [-@fig:012]).

![Имя узла](./image/12.png){#fig:012 width=70%}

Установил пароль для root (рис. [-@fig:013]).

![Пароль для root](./image/13.png){#fig:013 width=70%}

Задал пользователя и пароль (рис. [-@fig:014]).

![Пользователь](./image/14.png){#fig:014 width=70%}

Завершил установку (рис. [-@fig:015]).

![Завершение установки](./image/15.png){#fig:015 width=70%}

## Насторйка и проверка

Зашел в ОС под учетной записью (рис. [-@fig:016]).

![Вход](./image/16.png){#fig:016 width=70%}

Подключил образ гостевого диска (рис. [-@fig:017]).

![Подключение гостевой ОС](./image/17.png){#fig:017 width=70%}

В качестве проверки выполнил команду dmesg в терменале (рис. [-@fig:018]).

![Команда dmesg](./image/18.png){#fig:018 width=70%}

Выполнил команду dmesg | less (рис. [-@fig:019]).

![dmesg | less](./image/19.png){#fig:019 width=70%}

В пример выполнения задания выполнил команды dmesg | grep -i "CPU0" и dmesg | grep -i "Linux verison" (рис. [-@fig:020], [-@fig:021]).

![dmesg | grep -i "CPU0"](./image/20.png){#fig:020 width=70%}

![dmesg | grep -i "Linux verison"](./image/21.png){#fig:021 width=70%}

# Выводы

Приобрел практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Список литературы{.unnumbered}

::: {#refs}
:::
