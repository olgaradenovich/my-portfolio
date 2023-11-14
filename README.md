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
- Инструменты для машинного обучения: ``scikit-learn``, ``TensorFlow``



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

Задача: Проанализировать клиентский LTV по когортам и сделать выводы: какие когорты лучше, а какие хуже с точки зрения LTV.
<br> 
<p>Как решала: Построила сводную таблицу с абсолютным ретеншеном клиентов по месячным когортам. Построила таблицу с относительным базовым ретеншеном. На основании ретеншена рассчитала лайфтайм с помощью метода усредненных прямоугольников для каждой когорты. Рассчитала LTR для каждой когорты с помощью ARPU. Расположила значение ARPU в отдельной ячейке, чтобы на него было удобно ссылаться в вычислениях. Рассчитала LTV с помощью усредненных костов для каждой когорты.<p>
  
> <a href="https://github.com/olgaradenovich/my-portfolio/blob/main/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82_3.xlsx">Ссылка на проект</a>

  <p>Выводы (итоги): Сделаны выводы относительно хороших и плохих когорт с точки зрения LTV.<p>
<ol>
  <li>Итог №1: Выделена когорта, которая показывает высокий LTV за счет высокого лайфтайма - 01.05.2021</li>
  <li>Итог №2: Выделена когорта, которая показывает высокий LTV за счет низких костов - 01.11.2020</li>
  <li>Итог №3: Выделена когорта, которая показывает низкий LTV за счет низкого лайфтайма - 01.03.2021</li>
  <li>Итог №4: Выделена когорта, которая показывает низкий LTV за счет высоких костов - 01.01.2021</li>
</ol>

<br> 
<p>Проект 4: Построение витрины для модели машинного обучения в банке </p> 
<p>Что нужно было сделать: задача - Написать скрипт, который сделает витрину со следующими полями:

<ol>
  <li>Внутренний идентификатор клиента — поле id_client.</li>
<li>Название города — поле name_city из таблицы skybank.region_dict.</li>
<li>Числовой признак, который принимает значение 1 для мужчин и 0 для женщин — новое поле nflag_gender на основании поля gender.</li>
<li>Возраст — поле age.</li>
<li>Числовая переменная, которая показывает, в первый ли раз клиент обратился к нам за кредитом, — поле first_time.</li>
<li>Числовой признак, который принимает значение 1 при наличии мобильного телефона и 0 при его отсутствии — новое поле nflag_cellphone на основании поля cellphone.</li>
<li>Числовая переменная, которая показывает, активен ли клиент, — поле is_active.</li>
<li>Номер клиентского сегмента — поле cl_segm.</li>
<li>Размер выданного кредита — поле amt_loan.</li>
<li>Дата выдачи кредита — поле date_loan. Необходимо привести к формату даты.</li>
<li>Тип выданного кредита — поле credit_type.</li>
<li>Суммарный объем кредитов, выданных в этом городе.</li>
<li>Доля данного кредита среди всех кредитов, выданных в этом городе.</li>
<li>Суммарный объем кредитов, выданных в рамках указанного типа кредита.</li>
<li>Доля данного кредита среди всех кредитов, выданных в рамках указанного типа кредита.</li>
<li>Суммарный объем кредитов, выданных в рамках указанного типа кредита и города.</li>
<li>Доля данного кредита среди всех кредитов, выданных в рамках указанного типа кредита и города.</li>
<li>Количество кредитов, выданных в этом городе.</li>
<li>Количество кредитов, выданных в рамках указанного типа кредита.</li>
<li>Количество кредитов, выданных в рамках указанного типа кредита и города.</li>
</ol>
<p>
  
<p>Как решала: Для решения поставленной задачи я работала с таблицей skybank.late_collection_clients. Используя условный оператор CASE WHEN, функции SUM, COUNT, а также оператор LEFT JOIN для объединения двух таблиц, я написала необходимый скрипт.<p>

> <a href="https://github.com/olgaradenovich/my-portfolio/blob/main/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82_4.xlsx">Ссылка на проект</a>
  
 <p>Выводы (итоги): Подготовлена витрина для создания модели машинного обучения в банке.<p>

<br> 


<p>Проект 5: Моделирование изменения балансов студентов</p> 
<p>Что нужно было сделать:<p>
<ol>
  <li>Задача №1: Найти ответы на вопросы - сколько всего уроков было на балансе всех учеников за каждый календарный день и как это количество менялось под влиянием транзакций (оплат, начислений, корректирующих списаний) и уроков (списаний с баланса по мере прохождения уроков). Написать запрос, который собирает данные о балансах студентов за каждый "прожитый" ими день. </li>
  <li>Задача №2: Создать визуализацию (линейную диаграмму) итогового результата. Сделать выводы из получившейся визуализации?</li>
</ol>

<p>Как решала: Чтобы узнать, когда была первая транзакция для каждого студента, создала CTE `first_payments` с двумя полями: `user_id` и `first_payment_date` (дата первой успешной транзакции). Собрала таблицу с датами за каждый календарный день 2016 года. Выбрала все даты из таблицы `classes`, создадим CTE `all_dates` с полем `dt`, где будут храниться уникальные даты (без времени) уроков. Объединила таблицы и создала CTE `all_dates_by_user`, где будут храниться все даты жизни студента после того, как произошла его первая транзакция. Нашла все изменения балансов, связанные с успешными транзакциями. Выбрала все транзакции из таблицы `payments`, сгруппировала их по `user_id` и дате транзакции (без времени) и нашла сумму по полю `classes`. В результате получили CTE `payments_by_dates` с полями: `user_id`, `payment_date`, `transaction_balance_change` (сколько уроков было начислено или списано в этот день). Нашла баланс студентов, который сформирован только транзакциями. Для этого объединила `all_dates_by_user` и `payments_by_dates` так, чтобы совпадали даты и `user_id`. Использовала оконные выражения (функцию `sum`), чтобы найти кумулятивную сумму по полю `transaction_balance_change` для всех строк до текущей включительно с разбивкой по `user_id` и сортировкой по `dt`. В результате получили CTE `payments_by_dates_cumsum` с полями: `user_id`, `dt`, `transaction_balance_change` - `transaction_balance_change_cs` (кумулятивная сумма по `transaction_balance_change`). Нашла изменения балансов из-за прохождения уроков. Для этого создала CTE `classes_by_dates`, посчитав в таблице `classes` количество уроков за каждый день для каждого ученика. Получили результат с такими полями: `user_id`, `class_date`, `classes` (количество пройденных в этот день уроков). Причем `classes` умножила на `-1`, чтобы отразить, что `-` — это списания с баланса. Далее создала CTE для хранения кумулятивной суммы количества пройденных уроков. Для этого объединила таблицы `all_dates_by_user` и `classes_by_dates` так, чтобы совпадали даты и `user_id`. Используя оконные выражения (функцию `sum`), нашла кумулятивную сумму по полю `classes` для всех строк до текущей включительно с разбивкой по `user_id` и сортировкой по `dt`. В результате получили CTE `classes_by_dates_dates_cumsum`с полями: `user_id`, `dt`, `classes` — `classes_cs`(кумулятивная сумма по `classes`). Создала CTE `balances` с вычисленными балансами каждого студента. Для этого объединила таблицы `payments_by_dates_cumsum` и `classes_by_dates_dates_cumsum` так, чтобы совпадали даты и `user_id`. Чтобы узнать, как менялось общее количество уроков на балансах студентов, просуммировала поля `transaction_balance_change`, `transaction_balance_change_cs`, `classes`, `classes_cs`, `balance` из CTE `balances` с группировкой и сортировкой по `dt`. Создала визуализацию (линейную диаграмму) итогового результата и сформулировала выводы из получившейся визуализации?<p>

<image src="/pics/graph_2.jpg">

> <a href="https://github.com/olgaradenovich/my-portfolio/blob/main/%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82_5.xlsx">Ссылка на проект</a>
 
 <p>Выводы (итоги):<p>
<ol>
  <li>Итог №1: Написан запрос, который собирает данные о балансах студентов за каждый "прожитый" ими день. Выявлено, что студенты учатся "в долг", об этом гговорят отрицательные балансы. </li>
  <li>Итог №2: Создана визуализация. Из графика видно, что часть уроков осталась на балансе, они проплачены, но не пройдены. Пик оплат приходится на первые числа месяцев. В целом, отмечается рост продаж</li>
</ol>

## Контактная информация
- Email: name@email.com
- LinkedIn: https://www.linkedin.com/in/username/
- Личный сайт: https://www.username.com

