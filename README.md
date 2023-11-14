 # Портфолио: аналитик данных

## Обо мне 

Привет! Меня зовут ``Ольга Раденович``, я начинающий аналитик данных. 

В этом репозитории вы можете найти некоторые из моих проектов, выполненных во время обучения и практики.

## Навыки и технологии
<image src="/pics/Tools.jpg">
<br>
- Инструменты анализа данных: ``SQL``, ``Excel``: 
- Языки программирования и библиотеки: ``Python``, ``Pandas``, ``math`` 
- Системы управления базами данных: ``MySQL``, ``PostgreSQL``
- Средства визуализации данных: ``PowerBi``, ``Matplotlib``, ``seaborn``



## Проекты
<p> Проект 1: Калькулятор юнит-экономики онлайн-школы</p>
<p>Что нужно было сделать:<p>
<ol>
  <li>Задача №1. Просчитать на какую сумму мы могли бы увеличить расходы на основных сотрудников (Fixed costs / ФОТ) в апреле 2021 года при условии, что Маржинальность в этом месяце не должна упасть ниже 11%?</li>
  <li>Задача №2. Просчитать маржинальность за март 2021 года, если доля бесплатных уроков в нём упадёт на 10 процентных пунктов? P.S. При этом общее количество уроков не изменится - просто часть бесплатных уроков мы "продадим" за полную цену в 1 200 рублей? </li>
</ol>

<p>Как решала: Рассчитала юнит-калькулятор (CAC, ЗП Учителя на 1 урок, Fixed costs на 1 урок, Маржа). Затем, изменяя показатели маржи, просчитала изменение расходов на ФОТ, Lifetime Revenue (LTR) и маржинальность.<p>


> <a href="https://github.com/olgaradenovich/my-portfolio/blob/main/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82_1.xlsx">Ссылка на проект</a>

<p>Выводы (итоги):<p>
<ol>
  <li>Итог №1: При условии, что маржинальность в апреле 2021 года не должна упасть ниже 11%, мы могли бы увеличить расходы на основных сотрудников (Fixed costs / ФОТ) на 1 урок до 220,51 руб, т.е. на 45,46 руб</li>
  <li>Итог №2: Если бы бесплатных уроков было на ``10`` процентных пунктов меньше, а уроков за 1200 рублей на то же количество уроков больше, выручка увеличилась бы и составила 9 179 160 рублей. Маржинальность в марте 2021 года, пересчитанная с учётом уменьшившейся доли бесплатных уроков, составила бы 0,02% </li>
</ol>
<br> 

<p> Проект 2: Калькулятор юнит-экономики онлайн-кинотеатра</p>
<p>Что нужно было сделать:<p>
<ol>
  <li>Задача №1. Учесть в калькуляторе корректировку планов маркетинга </li>
  <li>Задача №2. Пересчитать план найма преподавателей </li>
</ol>

<p>Как решала: Добавила в список параметров калькулятора показатель «Поправочный коэффициент на привлечение». Установила значение этого показателя по умолчанию как 100% (в столбце «Факт для 05.21-04.22»). В столбец «План для 05.21-04.22» добавила формулу: в этом столбце меняется значение поправочного коэффициента, если меняется значение в столбце «Изменение». В столбце «Новые студенты» настроила динамический расчет количества новых студентов за период 05.21–04.22 с учетом поправочного коэффициента. Значения исходного количества студентов взяла на листе «План маркетинга». Для этого воспользовалась функцией ВПР(). Посчитала, сколько появится новых студентов за период 05.21–04.22, если значение поправочного коэффициента для периода станет 12% (настройки остальных показателей не меняются). Добавила в калькулятор на листе «Наём преподавателей» дополнительные столбцы: «Изменение» и «План». Это нужно, чтобы менять входные параметры: «Пропускную способность П» и «Retention П». Пересчитала общую пропускную способность. Изменила формулу так, чтобы отразить, что новые преподаватели могут проводить только половину уроков от средней пропускной способности преподавателя. С помощью функции ВПР() обновила прогнозное количество уроков на листе «Наём преподавателей», добавив значения из задачи 1 (полученные после перерасчета). Увеличила значение «Пропускной способности П» на 15%, а значение «Retention П» уменьшила на 2%. С помощью «Поиска решений» составила новый план найма с ограничением: за месяц нельзя нанять более 70 преподавателей.<p>

<image src="/pics/graph.jpg">

> <a href="https://github.com/olgaradenovich/my-portfolio/blob/main/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82_2.xlsx">Ссылка на проект</a>
 
<p>Выводы (итоги):<p>
<ol>
  <li>Итог №1: Обновленный лист с калькулятором + новое количество студентов на 04.2022.</li>
  <li>Итог №2: Обновленный план по найму с количеством новых преподавателей по месяцам за период с 05.2021 по 04.2022.</li>
</ol>
<br> 

<br> 
<p> Проект 3: Когортный анализ онлайн-кинотеатра с помощью SQL</p>
<p>Что нужно было сделать:<p>
<ol>
  <li>Задача №1</li>
  <li>Задача №2.</li>
</ol>

<p>Как решала(-а): краткое описание решения (автореферат)<p>
  
> <a href="https://drive.google.com/drive/folders/1wdD-mfSeIsHWgrMLJz8Tv_ClAuP_EAOQ?usp=sharing">Ссылка на проект</a>
(ссылка должна содержать демонстративные материалы: скриншоты, таблички, запросы, код. Работодатель должен иметь возможность быстро посмотреть результаты работы)

  <p>Выводы (итоги):<p>
<ol>
  <li>Итог №1</li>
  <li>Итог №2</li>
</ol>

<br> 
<p>Проект 4: Построение витрины для модели машинного обучения в банке </p> 
<p>Что нужно было сделать: задача №1.<p>
  
<p>Как решала(-а): краткое описание решения (автореферат)<p>

> <a href="https://drive.google.com/drive/folders/1QOk5AAh6x7jK_yHgfKI2sUFYR7AWUi5u">Ссылка на проект</a>
(ссылка должна содержать демонстративные материалы: скриншоты, таблички, запросы, код. Работодатель должен иметь возможность быстро посмотреть результаты работы)
  
 <p>Выводы (итоги):<p>
<ol>
  <li>Итог №1</li>
  <li>Итог №2</li>
</ol>
<br> 


<p>Проект 5: Моделирование изменения балансов студентов</p> 
<p>Что нужно было сделать:<p>
<ol>
  <li>Задача №1</li>
  <li>Задача №2.</li>
</ol>

<p>Как решала(-а): краткое описание решения (автореферат)<p>

> <a href="https://github.com/Skyproportfolio/data-analytics-5month/blob/main/Проект%205.xlsx">Ссылка на проект</a>
(ссылка должна содержать демонстративные материалы: скриншоты, таблички, запросы, код. Работодатель должен иметь возможность быстро посмотреть результаты работы)
 
 <p>Выводы (итоги):<p>
<ol>
  <li>Итог №1</li>
  <li>Итог №2</li>
</ol>

## Контактная информация
- Email: name@email.com
- LinkedIn: https://www.linkedin.com/in/username/
- Личный сайт: https://www.username.com

