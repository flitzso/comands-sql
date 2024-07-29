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

![01](https://github.com/user-attachments/assets/195c5b77-674d-478d-baf2-d0b85e7b590f)
![02](https://github.com/user-attachments/assets/6e78de27-1cb8-4375-975c-c42ccd2cd988)
![03](https://github.com/user-attachments/assets/989dab5b-2fd5-443f-8f50-1fd55ff8fc63)
![04](https://github.com/user-attachments/assets/b5fea6e4-5d41-4886-aac2-b020056c6eda)
![06](https://github.com/user-attachments/assets/0c75a3d1-94c5-4751-aa23-559ab4ee7f12)
![07](https://github.com/user-attachments/assets/f0b7435c-0cd3-4d64-864b-948014095f21)
![323896247_517345470385638_6798644583481855760_n](https://github.com/user-attachments/assets/96561078-6c93-4e7d-b46b-68ca5b9a4304)
![323925069_592115642747759_6513704659274634522_n](https://github.com/user-attachments/assets/43a48952-a53e-48e6-a527-4982537d04ae)
![323943896_1161830694536681_2750988523602349944_n](https://github.com/user-attachments/assets/735d1972-cf36-4240-9868-c864fc4ac4fd)
![323944768_478386801164210_5318695040946787334_n](https://github.com/user-attachments/assets/7484b590-dc5e-49da-8fc3-945c42f33951)
![324023984_434804432130718_8288419446737231785_n](https://github.com/user-attachments/assets/7802d86d-26eb-4494-aa50-e2e36c3aca36)
![324026210_1207888696824744_3231357974043022820_n](https://github.com/user-attachments/assets/f80bccf2-f30d-48a3-aceb-5cbd645ef029)
![324266156_1261592584394501_4763851286230674245_n](https://github.com/user-attachments/assets/11589e3e-6e33-4d02-b4e8-3ad3ecf3fa1b)
![324346888_1130824787611949_5405230067256485185_n](https://github.com/user-attachments/assets/480c8e47-5540-467c-ab5b-a18c5df12753)
![324583743_917958736050752_4991639231859468209_n](https://github.com/user-attachments/assets/c588b693-a156-4af9-9a47-094c9c812397)
![325887916_8636841349723630_910996207487369205_n](https://github.com/user-attachments/assets/af140c16-af90-4bf5-8a88-d8a3182809cc)
![325898864_601217891817780_4132979189320706182_n](https://github.com/user-attachments/assets/ebde4197-eaf0-4c2f-824b-148018bbb510)
![325907378_1074424856756786_3006536099257718666_n](https://github.com/user-attachments/assets/4f8bb166-f322-4ca5-b1b6-833b70456e8d)
![325976837_5590764574379709_7428688237701793620_n](https://github.com/user-attachments/assets/c2dd25ab-0510-40c7-b212-3acfa98f28ba)
![326095936_510147011229313_7123232748652381345_n](https://github.com/user-attachments/assets/7eb97bd7-70f1-40c3-a0e8-47c4c13882fd)
![326215113_877319733608847_8682966632322797353_n](https://github.com/user-attachments/assets/433baa63-1f84-423d-898e-1ab0f63d5189)
![326231002_474612694677207_8931919843183526466_n](https://github.com/user-attachments/assets/7b99adc2-0c2a-4935-aa48-4e596b84a9d3)
![326579246_1239083507011368_2741319493268554515_n](https://github.com/user-attachments/assets/6cb06588-3744-4ccf-9149-ff5a697384dd)




