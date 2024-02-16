!!! Пошаговые комментарии работы можно отследить в файле test-analytics-ubrr.ipynb

!!! CSV-таблицы с исходными данными расположены в архиве data.zip

!!! Задание "как есть" представлено в файле Test_BA.docx. Ниже текст задания, вынесенный отдельно в readme


Задание 1. Решить кейс.

Датасет test_analytics.csv  содержит данные по проведенным с клиентами банка коммуникациями по рекламным  маркетинговым кампаниям, цель которых предложить клиенту оформить кредит. Датасет также содержит данные по оформленным договорам после коммуникаций (поле fact =1 договор оформлен, fact = 0/Nan не оформлен). 

Необходимо проанализировать эффективность рекламных кампаний с клиентами на предложенных данных. Определить и рассчитать метрики эффективности. 
Эффективность оценить в разрезе кампаний (названия кампаний groups) . Описание сути кампаний представлено в таблице.

Сравнить эффективность каналов коммуникаций (comm_chanell), цепочек коммуникаций с клиентом в разрезе капании.
Посчитать стоимость выдачи (разные каналы сколько стоит 1 просмотр сколько стоит взятие кредита) и стоимость цепочек коммуникаций в разных каналах из расчета стоимости коммуникации с клиентом:

Успешный звонок 15 руб. 
SMS 4 руб. 
PUSH 0,2 руб.

(comm_status = 1 означает успешность коммуникации и оплачивается,  comm_status = 0 не дозвон, не оплачивается).

По итогам анализа дать рекомендации повышения эффективности рекламных кампаний.

Для выполнения задания использовать инструменты python. Результаты прислать в блокноте jupyter notebook с  текстовыми комментариями к вычислениям и итоговыми рекомендациями.

Задание 2. Написать запросы SQL. БД интернет-магазина фильмов и музыки. Прислать с текстовом файле.

1. Изучите заказы, которые оформили в сентябре 2011 года. Сравните общую сумму выручки (поле total) за каждый день этого месяца: выведите день в формате '2011-09-01' и сумму. Информацию о дате заказа хранит поле invoice_date. Оставьте в таблице только те значения суммы, которые больше 1 и меньше 10. Данные из таблицы invoice.

2. Посчитайте пропуски в поле с почтовым индексом billing_postal_code для каждой страны (поле billing_country). Получите срез: в таблицу должны войти только те записи, в которых поле billing_address не содержит слов Street, Way, Road или Drive. Отобразите в таблице страну и число пропусков, если их больше 10. Данные из таблицы invoice.  

3. Нужно объединить данные двух таблиц: track со всеми треками в магазине и invoice_line с купленными треками.  Выгрузите таблицу с названием трека и числом, которое соответствует тому, сколько раз трек покупали. Учитывайте, что в одном заказе один и тот же трек может встречаться несколько раз. Если какой-либо из треков не покупали или о купленном треке нет информации — такие записи не должны войти в таблицу. Оставьте только уникальные значения и отберите первые 20 записей.
