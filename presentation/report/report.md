---
## Front matter
title: "Операционные системы. Лекция 5"
subtitle: "Реферат на тему Trustworthy Computing Initiative"
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

# Введение

Trustworthy Computing (TWC, "Надежные вычисления") - это подход к созданию безопасных компьютерных систем, разработанный и популяризированный как инициатива Trustworthy Computing Initiative компанией Microsoft в 2002 году. 
Моей гипотезой является то, что инициатива TWC сделала UNIX-системы безопаснее. Обьект исследования - безопастность в UNIX-системах, предмет исследования - успешность использования TWC для защиты UNIX-систем.

# Актуальность

UNIX-системы часто используются для важных задач, требующих безопасности и конфидециальности:

- Корпоративные сервера
- Банковские системы
- Научные вычисления

Но они тоже могут быть уязвимы к атакам, даже в современном мире. Например, известные случаи с вирусами Code Red, Nimda and Slammer которые вдохновили Microsoft на создание TWC. Для того, чтобы заразить миллионы компьютеров, вирусу Nimda понадобилось всего 22 минуты. Конечно, есть и более современные случаи, например вирус-вымогатель Onyx, обнаруженный в 2022 году. Количество угроз растет каждый год, и именно поэтому сейчас как никогда актуальна тема поддержки инициативы TWC и разработки новых её аспектов. 

# Основные принципы TWC, заложенные в UNIX

Исторически, UNIX-системы разрабатывались с упором на безопастность, и поэтому в них были заложены многие принципы TWC. Четыре главных принципа, безопасность, конфедециальность, надежность и честность бизнеса, проявляются в многих аспектах UNIX-систем.

1. **Безопасность (Security)** - главный приоритет. В это входят минимальные привилегии и проактивная безопасность, например постоянный мониторинг и автоматизированное тестирование. Так, UNIX использует дискреционный (DAC) и мандатный (MAC, например, SELinux) контроль доступа, и утилизируют Firewall для защиты от сетевых атак.

2. **Конфиденциальность (Privacy)** - защита и обеспечение контроля над личными данными. В это входят многофакторная аутентификация, шифрование данных и детальный аудит. UNIX-системы поддерживают такие методы шифрования данных как LUKS, GPG и OpenSSL. Доступ к конфидециальным файлам можно контролировать встроенными командами chmod и chown.

3. **Надежность (Reliability)** - стабильная работа системы и минимизация сбоев. UNIX-системы известны своей устойчивостью (например, сервера на Linux).

4. **Честность бизнеса (Business integrity)** - прозрачность и ответственность компаний перед пользователями. Многие UNIX-системы (Linux, BSD) имеют открытый исходный код, а также стремятся соответствовать стандартам и иметь сертификации, например, FIPS (Federal Information Processing Standard), что повышает доверие пользователей. 

# Выводы и практическое применение

Опираясь на вышеперечисленные аспекты UNIX-систем, принципы Trustworthy Computing действительно делают их безопаснее. Но для максимальной эффективности я советую слушающим следующее:

1. Следить за обновлениями. Своевременное обновление системы гарантирует получение новых методов защиты от также новых угроз.

2. Настраивать права доступа и SSH-ключи. Осторожный подход к раздаче прав доступа к конфидециальным файлам и использование SELinux, а также использование SSH ключей вместо паролей устранят риск взлома или доступа других к важным данным.

3. Применять принципы TWC при разработке. Проектирование угрозы заранее, запуск программ с минимально нужными привелегиями, шифрование конфедициальных данных и проверка кода (Code review) на уязвимости, для которого есть заранее созданные инструменты, всё это сделает результат более безопасным. 

# Список литературы{.unnumbered}

::: {#refs}
:::

1. Публикация "Trustworthy Computing", Vijay Varadharajan, 2004 год (https://www.researchgate.net/publication/225171720_Trustworthy_Computing).

2. "Празднование двадцатилетия Trustworthy Computing", Аанчал Гупта, корпоративный вице-президент и заместитель директора по информационной безопасности Microsoft, 2022 год (https://www.microsoft.com/en-us/security/blog/2022/01/21/celebrating-20-years-of-trustworthy-computing/).

3. "Trustworthy Computing. Microsoft White Paper", Крэг Мунди, старший вице-президент по передовым стратегиям и курсам Microsoft (https://web.archive.org/web/20150626122214/http://download.microsoft.com/documents/australia/about/trustworthy_comp.doc)

4. Электронное письмо "Trustworthy Computing", Билл Гейтс, генеральный директор Microsoft, архив. 2002 год (https://web.archive.org/web/20150626172158/http://archive.wired.com/techbiz/media/news/2002/01/49826).

