---
## Front matter
title: "Персональный проект"
subtitle: "Шаг 1"
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

Установить Kali Linux


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

Задал имя машине и выбрал образ системы (рис. [-@fig:001]).

![Название](./image/01.png){#fig:001 width=70%}

Указал количество основной памяти и количество процессоров (рис. [-@fig:002]).

![Память](./image/02.png){#fig:002 width=70%}

Настроил размер жесткого диска (рис. [-@fig:003]).

![Диск](./image/03.png){#fig:003 width=70%}

Получил итоговую конфигурацию (рис. [-@fig:004]).

![Итог](./image/04.png){#fig:004 width=70%}

Начал установку ОС с выбора языка (рис. [-@fig:005]).

![Язык](./image/1.png){#fig:005 width=70%}

Выбрал язык раскладки (рис. [-@fig:006]).

![Раскладка](./image/2.png){#fig:006 width=70%}

Указал имя компьютера (рис. [-@fig:007]).

![Имя компьютера](./image/3.png){#fig:007 width=70%}

Указал имя домена (рис. [-@fig:008]).

![Имя домена](./image/4.png){#fig:008 width=70%}

Указал имя учетной записи (рис. [-@fig:009]).

![Имя учетной записи](./image/5.png){#fig:009 width=70%}

Указал имя пользователя (рис. [-@fig:010]).

![Имя учетной пользователя](./image/6.png){#fig:010 width=70%}

Создал парль (рис. [-@fig:011]).

![Параль](./image/7.png){#fig:011 width=70%}

Выбрал часовой пояс (рис. [-@fig:012]).

![Часовой пояс](./image/8.png){#fig:012 width=70%}

Выбрал автоматеческую разметку дисков (рис. [-@fig:013]).

![Разметка диска](./image/9.png){#fig:013 width=70%}

Выбрал конкретный диск (рис. [-@fig:014]).

![Диск](./image/10.png){#fig:014 width=70%}

Выбрал конкретную схему разметки (рис. [-@fig:015]).

![Схема разметки](./image/11.png){#fig:015 width=70%}

Выбрал программное обеспечение (рис. [-@fig:016]).

![ПО](./image/14.png){#fig:016 width=70%}

Настроил менеджер дисплеев (рис. [-@fig:017]).

![Менеджер дисплеев](./image/15.png){#fig:017 width=70%}

Завершил установку ОС (рис. [-@fig:017]).

![Конец](./image/16.png){#fig:017 width=70%}
.
# Выводы

Установил Kali Linux на свою виртуальную машину

# Список литературы{.unnumbered}

::: {#refs}
:::
