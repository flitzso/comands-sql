+-------------+<br />
|  Tabela PK  |<br />
+-------------+<br />

CREATE TABLE clientes (<br />
    id INT NOT NULL AUTO_INCREMENT,<br />
    nome VARCHAR(50),<br />
    telefone VARCHAR(15),<br />
    email VARCHAR(50),<br />
    PRIMARY KEY (id)<br />
);<br />

+-------------+<br />
|  Tabela FK  |<br />
+-------------+<br />

CREATE TABLE pedidos (<br />
    id INT NOT NULL AUTO_INCREMENT,<br />
    data_pedido DATE,<br />
    valor_total DECIMAL(10,2),<br />
    PRIMARY KEY (id)<br />
);<br />

CREATE TABLE itens_pedido (<br />
    id INT NOT NULL AUTO_INCREMENT,<br />
    id_pedido INT,<br />
    nome_produto VARCHAR(50),<br />
    quantidade INT,<br />
    valor_unitario DECIMAL(10,2),<br />
    PRIMARY KEY (id),<br />
    FOREIGN KEY (id_pedido) REFERENCES pedidos(id)<br />
);<br />

+-------------+<br />
|   Consulta  |<br />
+-------------+<br />

SELECT coluna1, coluna2, ...<br />
FROM nome_tabela<br />
WHERE condicao;<br />
+-------------------------+<br />
SELECT * FROM clientes;<br />
+-------------------------+<br />
SELECT nome, telefone<br />
FROM clientes<br />
WHERE email = 'exemplo@email.com';<br />

+--------------------------------------------+<br />
|  Adicionar - Alterar - Selecionar - Deletar |<br />
+--------------------------------------------+<br />

Adicionar:<br />

INSERT INTO clientes (nome, telefone, email)<br />
VALUES ('João', '555-1234', 'joao@email.com');<br />
+---------------------------------------------+<br />
Alterar:<br />

UPDATE nome_tabela<br />
SET coluna1 = valor1, coluna2 = valor2, ...<br />
WHERE condicao;<br />

UPDATE clientes<br />
SET telefone = '555-5678'<br />
WHERE nome = 'João';<br />
+---------------------------------------------+<br />
Selecionar:<br />

SELECT nome, telefone, email<br />
FROM clientes;<br />
+---------------------------------------------+<br />
Deletar:<br />

DELETE FROM nome_tabela<br />
WHERE condicao;<br />

DELETE FROM clientes<br />
WHERE nome = 'João';<br />

+-------------------------------------------------------+<br />
| SEMPRE MUITA ATENÇÃO AO DELETAR ALGO USE O SELECT ANTES |<br />
+-------------------------------------------------------+<br />
