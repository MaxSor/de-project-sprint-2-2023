# de-project-sprint-2-2023
По замечанию к строке `RANK() OVER(PARTITION BY T2.customer_id ORDER BY count_product DESC) AS rank_count_product`
Да, будут дубли, но они убираются условием `WHERE T4.rank_craftsman_id = 1 AND T4.rank_count_product = 1 ORDER BY report_period -- условие помогает оставить в выборке первую по популярности категорию товаров и самого популярного мастера`
Очень неудобно что в тестовых данных нет случаев где хотя бы у одного клиента больше 1 заказа с одной и той же категорией или мастером.