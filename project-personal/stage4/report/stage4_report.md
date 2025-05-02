---
## Front matter
title: "Индивидуальный проект, этап 4"
subtitle: "Дисциплина - Операционные Системы"
author: "Азарцова Вероника Валерьевна"

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

Продолжить работы с личным сайтом на Github pages.

# Задание

1. Добавить ссылки на сайты.

2. Сделать посты:
   - Сделать пост по прошедшей неделе
   - Добавить пост на тему по выбору: Оформление отчёта; Создание презентаций; Работа с библиографией.

# Теоретическое введение

Hugo Blox Builder — это фреймворк без кода для создания любого типа веб-сайта с использованием виджетов.  
Он позволяет писать контент, используя стандартизированный Markdown вместе с пакетными расширениями для математики и диаграмм, и редактируйте в CMS с открытым исходным кодом или через редактор, такой как онлайн-редактор GitHub, Jupyter Notebook или RStudio.  

# Выполнение лабораторной работы
1. Добавляю ссылки на сайты (рис. [-@fig:1], [-@fig:2])

- eLibrary : https://elibrary.ru/;

- Google Scholar : https://scholar.google.com/;

- ORCID : https://orcid.org/;

- Mendeley : https://www.mendeley.com/;

- ResearchGate : https://www.researchgate.net/;

- Academia.edu : https://www.academia.edu/;

- arXiv : https://arxiv.org/;

- github : https://github.com/.

![index.md сайта](image/1.png){#fig:1 width=70%}

![Ссылки (ярлыки) на сайте](image/2.png){#fig:2 width=70%}

2. Создаю пост о прошедшей неделе (рис. [-@fig:3], [-@fig:4]).

![index.md первого поста](image/3.png){#fig:3 width=70%}

![Первый пост на сайте](image/4.png){#fig:4 width=70%}

3. Создаю пост о создании презентаций (рис. [-@fig:5], [-@fig:6]).

![index.md второго поста](image/5.png){#fig:5 width=70%}

![Второй пост на сайте](image/6.png){#fig:6 width=70%}

# Выводы

Подводя итоги проведенной проектной работе, я дополнила мой сайт ссылками, и создала два поста: о моей неделе, и о языке создании презентаций, тем самым закрепив мои навыки работы с Hugo.


# Список литературы{.unnumbered}

::: {#refs}
:::
