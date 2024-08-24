# Comandos SQL

## SQL Command Examples and Documentation

Este repositório contém uma documentação detalhada e exemplos práticos de comandos SQL frequentemente utilizados em desenvolvimento de bancos de dados. O objetivo deste repositório é servir como uma referência rápida para desenvolvedores, estudantes e profissionais que trabalham com SQL, permitindo um entendimento claro e aplicação eficiente dos comandos.

### Estrutura do Repositório

- **Documentação de Comandos SQL**: Um arquivo Markdown que descreve e explica cada comando SQL, com uma visão geral e exemplos de uso.
- **Exemplos de Comandos SQL**: Um arquivo separado contendo apenas os exemplos práticos de cada comando SQL, organizados por tópicos.

### Comandos SQL Cobertos


## Este repositório cobre uma ampla gama de comandos SQL, incluindo, mas não se limitando a:

- **Filtros e Condições**: `BETWEEN`, `IN`, `AND`, `LIKE`, `iLIKE`, `CASE`
- **Funções de Agregação**: `COUNT`, `MAX`, `MIN`, `AVG`, `SUM`
- **Ordenação e Limitação de Resultados**: `ORDER BY`, `LIMIT`, `OFFSET`, `FETCH`
- **Agrupamento e Filtragem de Grupos**: `GROUP BY`, `HAVING`
- **Manipulação de Strings**: `LIKE`, `iLIKE`, `%`, `_`
- **Tratamento de Nulos**: `COALESCE`, `NULLIF`
- **Conexão de Tabelas**: `JOIN`, `LEFT JOIN`, `INNER JOIN`, `RIGHT JOIN`, `FULL OUTER JOIN`
- **Combinação de Resultados**: `UNION`, `UNION ALL`
- **Outras Funções e Comandos**: `EXTRACT`, `AGE`, `CONSTRAINT`, `UNIQUE`, `ON CONFLICT DO NOTHING`, `ON CONFLICT UPDATE SET`, `CAST`, `TRUNCATE`, `DELETE`, `INSERT`, `UPDATE`, `ALTER TABLE`, `DROP TABLE`, `CREATE TABLE`, `PRIMARY KEY`, `FOREIGN KEY`, `CHECK`


## Índice

- [DISTINCT](#distinct)
- [OFFSET](#offset)
- [LIMIT](#limit)
- [FETCH](#fetch)
- [IN](#in)
- [AND](#and)
- [LIKE](#like)
- [iLIKE](#ilike)
- ['_____'](#_____)
- ['%'](#percent)
- [COUNT](#count)
- [ORDER BY](#order-by)
- [GROUP BY](#group-by)
- [DESC](#desc)
- [ASC](#asc)
- [HAVING](#having)
- [MAX](#max)
- [MIN](#min)
- [AVG](#avg)
- [ROUND](#round)
- [SUM](#sum)
- [ALIAS](#alias)
- [COALESCE](#coalesce)
- [NULLIF](#nullif)
- [EXTRACT](#extract)
- [AGE](#age)
- [CONSTRAINT](#constraint)
- [UNIQUE](#unique)
- [ON CONFLICT DO NOTHING](#on-conflict-do-nothing)
- [ON CONFLICT UPDATE SET](#on-conflict-update-set)
- [JOIN](#join)
- [LEFT JOIN](#left-join)
- [INNER JOIN](#inner-join)
- [RIGHT JOIN](#right-join)
- [FULL OUTER JOIN](#full-outer-join)
- [UNION](#union)
- [UNION ALL](#union-all)
- [CASE](#case)
- [CAST](#cast)
- [TRUNCATE](#truncate)
- [DELETE](#delete)
- [INSERT](#insert)
- [UPDATE](#update)
- [ALTER TABLE](#alter-table)
- [DROP TABLE](#drop-table)
- [CREATE TABLE](#create-table)
- [PRIMARY KEY](#primary-key)
- [FOREIGN KEY](#foreign-key)
- [CHECK](#check)

---

## Descrições de Comandos SQL

### DISTINCT
O comando `DISTINCT` é usado para retornar apenas valores distintos, eliminando duplicatas.

### OFFSET
O comando `OFFSET` é utilizado para ignorar um número específico de linhas antes de começar a retornar as linhas de resultado.

### LIMIT
O comando `LIMIT` limita o número de linhas retornadas por uma consulta.

### FETCH
O comando `FETCH` é usado em conjunto com `OFFSET` para limitar o número de linhas retornadas.

### IN
O comando `IN` é utilizado para filtrar resultados que correspondem a qualquer valor dentro de um conjunto especificado.

### AND
O comando `AND` é usado para combinar condições múltiplas em uma cláusula `WHERE`.

### LIKE
O comando `LIKE` é usado para buscar um padrão específico em uma coluna.

### iLIKE
O comando `iLIKE` é semelhante ao `LIKE`, mas não diferencia maiúsculas de minúsculas.

### '_____'
O uso de `'_____'` com `LIKE` permite buscar valores que correspondem exatamente a um número de caracteres.

### '%'
O caractere `%` com `LIKE` ou `iLIKE` é usado para substituir qualquer sequência de caracteres.

### COUNT
O comando `COUNT` retorna o número total de linhas que correspondem ao critério especificado.

### ORDER BY
O comando `ORDER BY` é usado para ordenar os resultados da consulta.

### GROUP BY
O comando `GROUP BY` é utilizado para agrupar linhas que têm valores em colunas específicas em comum.

### DESC
O modificador `DESC` é usado com `ORDER BY` para ordenar os resultados em ordem decrescente.

### ASC
O modificador `ASC` é usado com `ORDER BY` para ordenar os resultados em ordem crescente.

### HAVING
O comando `HAVING` é utilizado para filtrar os resultados de grupos formados pelo `GROUP BY`.

### MAX
O comando `MAX` retorna o valor máximo de uma coluna.

### MIN
O comando `MIN` retorna o valor mínimo de uma coluna.

### AVG
O comando `AVG` retorna a média dos valores de uma coluna.

### ROUND
O comando `ROUND` é utilizado para arredondar um valor numérico.

### SUM
O comando `SUM` retorna a soma de todos os valores em uma coluna.

### ALIAS
`ALIAS` é utilizado para renomear colunas ou tabelas para simplificar a leitura do código.

### COALESCE
O comando `COALESCE` retorna o primeiro valor não nulo em uma lista de argumentos.

### NULLIF
O comando `NULLIF` compara dois valores e retorna `NULL` se forem iguais, caso contrário, retorna o primeiro valor.

### EXTRACT
O comando `EXTRACT` é utilizado para extrair uma subparte de uma data ou intervalo.

### AGE
O comando `AGE` calcula a diferença entre duas datas.

### CONSTRAINT
O comando `CONSTRAINT` é utilizado para definir restrições em colunas ou tabelas.

### UNIQUE
A restrição `UNIQUE` garante que todos os valores em uma coluna ou conjunto de colunas sejam distintos.

### ON CONFLICT DO NOTHING
O comando `ON CONFLICT DO NOTHING` permite ignorar conflitos de inserção, como uma duplicação de chave.

### ON CONFLICT UPDATE SET
O comando `ON CONFLICT UPDATE SET` permite que, em caso de conflito, os valores sejam atualizados.

### JOIN
O comando `JOIN` combina linhas de duas ou mais tabelas com base em uma condição relacionada.

### LEFT JOIN
O comando `LEFT JOIN` retorna todas as linhas da tabela à esquerda, e as linhas correspondentes da tabela à direita. Se não houver correspondência, o resultado conterá `NULL` para as colunas da tabela à direita.

### INNER JOIN
O comando `INNER JOIN` retorna todas as linhas que têm correspondências em ambas as tabelas.

### RIGHT JOIN
O comando `RIGHT JOIN` retorna todas as linhas da tabela à direita, e as linhas correspondentes da tabela à esquerda. Se não houver correspondência, o resultado conterá `NULL` para as colunas da tabela à esquerda.

### FULL OUTER JOIN
O comando `FULL OUTER JOIN` retorna todas as linhas quando há uma correspondência em uma das tabelas. Se não houver correspondência, o resultado conterá `NULL` para as colunas da tabela que não tem correspondência.

### UNION
O comando `UNION` combina os resultados de duas ou mais consultas `SELECT`, retornando apenas valores distintos.

### UNION ALL
O comando `UNION ALL` combina os resultados de duas ou mais consultas `SELECT`, incluindo duplicatas.

### CASE
O comando `CASE` permite realizar operações condicionais em consultas SQL.

### CAST
O comando `CAST` converte um valor de um tipo de dado para outro.

### TRUNCATE
O comando `TRUNCATE` remove todas as linhas de uma tabela de maneira rápida e eficiente, sem gerar logs de transação.

### DELETE
O comando `DELETE` é usado para remover linhas de uma tabela com base em uma condição.

### INSERT
O comando `INSERT` é usado para adicionar novas linhas a uma tabela.

### UPDATE
O comando `UPDATE` é usado para modificar os dados existentes em uma tabela.

### ALTER TABLE
O comando `ALTER TABLE` é usado para modificar a estrutura de uma tabela existente, como adicionar, remover ou alterar colunas.

### DROP TABLE
O comando `DROP TABLE` é usado para remover uma tabela do banco de dados.

### CREATE TABLE
O comando `CREATE TABLE` é usado para criar uma nova tabela no banco de dados.

### PRIMARY KEY
A restrição `PRIMARY KEY` identifica de forma exclusiva cada registro em uma tabela.

### FOREIGN KEY
A restrição `FOREIGN KEY` cria um vínculo entre duas tabelas, garantindo a integridade referencial dos dados.

### CHECK
A restrição `CHECK` é usada para limitar os valores que podem ser colocados em uma coluna.

