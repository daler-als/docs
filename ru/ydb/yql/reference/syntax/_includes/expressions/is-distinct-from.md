---
sourcePath: ru/ydb/ydb-docs-core/ru/core/yql/reference/yql-core/syntax/_includes/expressions/is-distinct-from.md
sourcePath: ru/ydb/yql/reference/yql-core/syntax/_includes/expressions/is-distinct-from.md
---
## IS \[NOT\] DISTINCT FROM {#is-distinct-from}

Сравнение двух значений. В отличие от обычных [операторов сравнения](#comparison-operators), нуллы считаются равными друг другу.
Точнее говоря, сравнение осуществляется по следующим правилам:
1) операторы `IS DISTINCT FROM`/`IS NOT DISTINCT FROM` определены для тех и только для тех аргументов, для которых определены операторы `!=` и `=`;
2) результат `IS NOT DISTINCT FROM` равен логическому отрицанию результата `IS DISTINCT FROM` для данных аргументов;
3) если результат оператора `==` не равен нуллу для некоторых аргументов, то он совпадает с результатом оператора `IS NOT DISTINCT FROM` для тех же аргументов;
4) если оба аргумента являются незаполненными `Optional`ми или `NULL`ами, то значение `IS NOT DISTINCT FROM` равно  `True`
5) результат `IS NOT DISTINCT FROM` от незаполненного `Optional` или `NULL` и заполненного `Optional` или не-`Optional` значения равен `False`.

Для значений композитных типов эти правила применяются рекурсивно.