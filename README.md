# Comandos SQL

## SQL Command Examples and Documentation

Este repositório contém uma documentação detalhada e exemplos práticos de comandos SQL frequentemente utilizados em desenvolvimento de bancos de dados. O objetivo deste repositório é servir como uma referência rápida para desenvolvedores, estudantes e profissionais que trabalham com SQL, permitindo um entendimento claro e aplicação eficiente dos comandos.

### Estrutura do Repositório

- **Documentação de Comandos SQL**: Um arquivo Markdown que descreve e explica cada comando SQL, com uma visão geral e exemplos de uso.
- **Exemplos de Comandos SQL**: Um arquivo separado contendo apenas os exemplos práticos de cada comando SQL, organizados por tópicos.

### Comandos SQL Cobertos


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
- [BETWEEN](#between)

---

## Descrições de Comandos SQL

### '%'
- **Comando:** `%`
  - **Descrição:** Usado com `LIKE` ou `iLIKE` para substituir qualquer sequência de caracteres.
  - **Exemplo:**
    ```sql
    SELECT * FROM clientes WHERE email LIKE '%@gmail.com';
    ```

### '_____'
- **Comando:** `'_____'`
  - **Descrição:** Com `LIKE`, permite buscar valores que correspondem exatamente a um número de caracteres.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos WHERE codigo LIKE 'ABCD_';
    ```

### AGE
- **Comando:** `AGE`
  - **Descrição:** Calcula a diferença entre duas datas.
  - **Exemplo:**
    ```sql
    SELECT AGE(data_nascimento) FROM clientes;
    ```

### ALIAS
- **Comando:** `ALIAS`
  - **Descrição:** Renomeia colunas ou tabelas para simplificar a leitura do código.
  - **Exemplo:**
    ```sql
    SELECT preco AS valor, nome AS produto FROM produtos;
    ```

### ALTER TABLE
- **Comando:** `ALTER TABLE`
  - **Descrição:** Modifica a estrutura de uma tabela existente, como adicionar, remover ou alterar colunas.
  - **Exemplo:**
    ```sql
    ALTER TABLE produtos ADD COLUMN estoque INT;
    ```

### AND
- **Comando:** `AND`
  - **Descrição:** Combina condições múltiplas em uma cláusula `WHERE`.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos WHERE preco > 10 AND estoque > 0;
    ```

### ASC
- **Comando:** `ASC`
  - **Descrição:** Usado com `ORDER BY` para ordenar os resultados em ordem crescente.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos ORDER BY preco ASC;
    ```

### BETWEEN
- **Comando:** `BETWEEN`
  - **Descrição:** O comando `BETWEEN` é usado para filtrar os resultados dentro de um intervalo especificado, incluindo os valores de limite.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos WHERE preco BETWEEN 10 AND 20;
    ```

### CASE
- **Comando:** `CASE`
  - **Descrição:** Permite realizar operações condicionais em consultas SQL.
  - **Exemplo:**
    ```sql
    SELECT nome, 
           CASE 
               WHEN preco > 100 THEN 'Caro' 
               ELSE 'Barato' 
           END AS categoria_preco
    FROM produtos;
    ```

### CAST
- **Comando:** `CAST`
  - **Descrição:** Converte um valor de um tipo de dado para outro.
  - **Exemplo:**
    ```sql
    SELECT CAST(preco AS INTEGER) FROM produtos;
    ```

### CHECK
- **Comando:** `CHECK`
  - **Descrição:** Limita os valores que podem ser colocados em uma coluna.
  - **Exemplo:**
    ```sql
    CREATE TABLE produtos (
        id SERIAL PRIMARY KEY,
        preco DECIMAL(10, 2) CHECK (preco > 0)
    );
    ```

### CONSTRAINT
- **Comando:** `CONSTRAINT`
  - **Descrição:** Define restrições em colunas ou tabelas.
  - **Exemplo:**
    ```sql
    ALTER TABLE produtos ADD CONSTRAINT chk_preco CHECK (preco > 0);
    ```

### COALESCE
- **Comando:** `COALESCE`
  - **Descrição:** Retorna o primeiro valor não nulo em uma lista de argumentos.
  - **Exemplo:**
    ```sql
    SELECT COALESCE(desconto, 0) FROM vendas;
    ```

### COUNT
- **Comando:** `COUNT`
  - **Descrição:** Retorna o número total de linhas que correspondem ao critério especificado.
  - **Exemplo:**
    ```sql
    SELECT COUNT(*) FROM produtos WHERE preco > 20;
    ```

### CREATE TABLE
- **Comando:** `CREATE TABLE`
  - **Descrição:** Cria uma nova tabela no banco de dados.
  - **Exemplo:**
    ```sql
    CREATE TABLE produtos (
        id SERIAL PRIMARY KEY,
        nome VARCHAR(255),
        preco DECIMAL(10, 2)
    );
    ```

### DELETE
- **Comando:** `DELETE`
  - **Descrição:** Remove linhas de uma tabela com base em uma condição.
  - **Exemplo:**
    ```sql
    DELETE FROM produtos WHERE preco < 10;
    ```

### DESC
- **Comando:** `DESC`
  - **Descrição:** Usado com `ORDER BY` para ordenar os resultados em ordem decrescente.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos ORDER BY preco DESC;
    ```

### DISTINCT
- **Comando:** `DISTINCT`
  - **Descrição:** Retorna apenas valores distintos, eliminando duplicatas.
  - **Exemplo:**
    ```sql
    SELECT DISTINCT categoria FROM produtos;
    ```

### DROP TABLE
- **Comando:** `DROP TABLE`
  - **Descrição:** Remove uma tabela do banco de dados.
  - **Exemplo:**
    ```sql
    DROP TABLE produtos;
    ```

### EXTRACT
- **Comando:** `EXTRACT`
  - **Descrição:** Extrai uma subparte de uma data ou intervalo.
  - **Exemplo:**
    ```sql
    SELECT EXTRACT(YEAR FROM data_venda) FROM vendas;
    ```

### FETCH
- **Comando:** `FETCH`
  - **Descrição:** Usado em conjunto com `OFFSET` para limitar o número de linhas retornadas.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos ORDER BY preco ASC OFFSET 5 FETCH NEXT 10 ROWS ONLY;
    ```

### FOREIGN KEY
- **Comando:** `FOREIGN KEY`
  - **Descrição:** Cria um vínculo entre duas tabelas, garantindo a integridade referencial dos dados.
  - **Exemplo:**
    ```sql
    CREATE TABLE pedidos (
        id SERIAL PRIMARY KEY,
        cliente_id INT REFERENCES clientes(id)
    );
    ```

### FULL OUTER JOIN
- **Comando:** `FULL OUTER JOIN`
  - **Descrição:** Retorna todas as linhas quando há uma correspondência em uma das tabelas. Se não houver correspondência, o resultado conterá `NULL` para as colunas da tabela que não tem correspondência.
  - **Exemplo:**
    ```sql
    SELECT * FROM pedidos FULL OUTER JOIN clientes ON pedidos.cliente_id = clientes.id;
    ```

### GROUP BY
- **Comando:** `GROUP BY`
  - **Descrição:** Agrupa linhas que têm valores em colunas específicas em comum.
  - **Exemplo:**
    ```sql
    SELECT categoria, COUNT(*) FROM produtos GROUP BY categoria;
    ```

### HAVING
- **Comando:** `HAVING`
  - **Descrição:** Filtra os resultados de grupos formados pelo `GROUP BY`.
  - **Exemplo:**
    ```sql
    SELECT categoria, COUNT(*) FROM produtos GROUP BY categoria HAVING COUNT(*) > 5;
    ```

### IN
- **Comando:** `IN`
  - **Descrição:** Filtra resultados que correspondem a qualquer valor dentro de um conjunto especificado.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos WHERE categoria IN ('Eletrônicos', 'Móveis');
    ```

### INNER JOIN
- **Comando:** `INNER JOIN`
  - **Descrição:** Retorna todas as linhas que têm correspondências em ambas as tabelas.
  - **Exemplo:**
    ```sql
    SELECT * FROM pedidos INNER JOIN clientes ON pedidos.cliente_id = clientes.id;
    ```

### INSERT
- **Comando:** `INSERT`
  - **Descrição:** Adiciona novas linhas a uma tabela.
  - **Exemplo:**
    ```sql
    INSERT INTO produtos (nome, preco) VALUES ('Produto A', 20.0);
    ```

### iLIKE
- **Comando:** `iLIKE`
  - **Descrição:** Similar ao `LIKE`, mas não diferencia maiúsculas de minúsculas.
  - **Exemplo:**
    ```sql
    SELECT * FROM clientes WHERE nome iLIKE 'joão%';
    ```

### JOIN
- **Comando:** `JOIN`
  - **Descrição:** Combina linhas de duas ou mais tabelas com base em uma condição relacionada.
  - **Exemplo:**
    ```sql
    SELECT * FROM pedidos JOIN clientes ON pedidos.cliente_id = clientes.id;
    ```

### LEFT JOIN
- **Comando:** `LEFT JOIN`
  - **Descrição:** Retorna todas as linhas da tabela à esquerda, e as linhas correspondentes da tabela à direita. Se não houver correspondência, o resultado conterá `NULL` para as colunas da tabela à direita.
  - **Exemplo:**
    ```sql
    SELECT * FROM pedidos LEFT JOIN clientes ON pedidos.cliente_id = clientes.id;
    ```

### LIKE
- **Comando:** `LIKE`
  - **Descrição:** Busca um padrão específico em uma coluna.
  - **Exemplo:**
    ```sql
    SELECT * FROM clientes WHERE nome LIKE 'João%';
    ```

### LIMIT
- **Comando:** `LIMIT`
  - **Descrição:** Limita o número de linhas retornadas por uma consulta.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos LIMIT 10;
    ```

### MAX
- **Comando:** `MAX`
  - **Descrição:** Retorna o valor máximo de uma coluna.
  - **Exemplo:**
    ```sql
    SELECT MAX(preco) FROM produtos;
    ```

### MIN
- **Comando:** `MIN`
  - **Descrição:** Retorna o valor mínimo de uma coluna.
  - **Exemplo:**
    ```sql
    SELECT MIN(preco) FROM produtos;
    ```

### NULLIF
- **Comando:** `NULLIF`
  - **Descrição:** Compara dois valores e retorna `NULL` se forem iguais, caso contrário, retorna o primeiro valor.
  - **Exemplo:**
    ```sql
    SELECT NULLIF(preco_promocional, preco_normal) FROM produtos;
    ```

### OFFSET
- **Comando:** `OFFSET`
  - **Descrição:** Ignora um número específico de linhas antes de começar a retornar as linhas de resultado.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos ORDER BY preco ASC OFFSET 5;
    ```

### ON CONFLICT DO NOTHING
- **Comando:** `ON CONFLICT DO NOTHING`
  - **Descrição:** Ignora conflitos de inserção, como uma duplicação de chave.
  - **Exemplo:**
    ```sql
    INSERT INTO usuarios (email) VALUES ('teste@teste.com')
    ON CONFLICT DO NOTHING;
    ```

### ON CONFLICT UPDATE SET
- **Comando:** `ON CONFLICT UPDATE SET`
  - **Descrição:** Em caso de conflito, os valores são atualizados.
  - **Exemplo:**
    ```sql
    INSERT INTO produtos (id, nome, preco) VALUES (1, 'Produto A', 20.0)
    ON CONFLICT (id) DO UPDATE SET preco = 20.0;
    ```

### ORDER BY
- **Comando:** `ORDER BY`
  - **Descrição:** Ordena os resultados da consulta.
  - **Exemplo:**
    ```sql
    SELECT * FROM produtos ORDER BY preco DESC;
    ```

### PRIMARY KEY
- **Comando:** `PRIMARY KEY`
  - **Descrição:** Identifica de forma exclusiva cada registro em uma tabela.
  - **Exemplo:**
    ```sql
    CREATE TABLE usuarios (
        id SERIAL PRIMARY KEY,
        email VARCHAR(255)
    );
    ```

### RIGHT JOIN
- **Comando:** `RIGHT JOIN`
  - **Descrição:** Retorna todas as linhas da tabela à direita, e as linhas correspondentes da tabela à esquerda. Se não houver correspondência, o resultado conterá `NULL` para as colunas da tabela à esquerda.
  - **Exemplo:**
    ```sql
    SELECT * FROM pedidos RIGHT JOIN clientes ON pedidos.cliente_id = clientes.id;
    ```

### ROUND
- **Comando:** `ROUND`
  - **Descrição:** Arredonda um valor numérico.
  - **Exemplo:**
    ```sql
    SELECT ROUND(AVG(preco), 2) FROM produtos;
    ```

### SUM
- **Comando:** `SUM`
  - **Descrição:** Retorna a soma de todos os valores em uma coluna.
  - **Exemplo:**
    ```sql
    SELECT SUM(quantidade) FROM vendas;
    ```

### TRUNCATE
- **Comando:** `TRUNCATE`
  - **Descrição:** Remove todas as linhas de uma tabela de maneira rápida e eficiente, sem gerar logs de transação.
  - **Exemplo:**
    ```sql
    TRUNCATE TABLE produtos;
    ```

### UNION
- **Comando:** `UNION`
  - **Descrição:** Combina os resultados de duas ou mais consultas `SELECT`, retornando apenas valores distintos.
  - **Exemplo:**
    ```sql
    SELECT nome FROM clientes UNION SELECT nome FROM fornecedores;
    ```

### UNION ALL
- **Comando:** `UNION ALL`
  - **Descrição:** Combina os resultados de duas ou mais consultas `SELECT`, incluindo duplicatas.
  - **Exemplo:**
    ```sql
    SELECT nome FROM clientes UNION ALL SELECT nome FROM fornecedores;
    ```

### UNIQUE
- **Comando:** `UNIQUE`
  - **Descrição:** Garante que todos os valores em uma coluna ou conjunto de colunas sejam distintos.
  - **Exemplo:**
    ```sql
    CREATE TABLE usuarios (
        id SERIAL PRIMARY KEY,
        email VARCHAR(255) UNIQUE
    );
    ```

### UPDATE
- **Comando:** `UPDATE`
  - **Descrição:** Modifica os dados existentes em uma tabela.
  - **Exemplo:**
    ```sql
    UPDATE produtos SET preco = preco * 1.1 WHERE categoria = 'Eletrônicos';
    ```


