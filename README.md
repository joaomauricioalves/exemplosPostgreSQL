<h1>Olá Mundo!!</h1>

<h2>Exemplo 1</h2>

Você é funcionário da SeVira Solutions, uma empresa faz tudo na área de TI. Ela foi contratada para abolir o uso de planilhas em uma loja de instrumentos musicais.

A sua tarefa já foi delegada pela equipe de desenvolvimento, que será importar um arquivo chamado orcamento.csv para um banco de dados do PostgreSQL. 

Então você aceita o desafio?

- Vamos criar um Database chamado orcamento

- Criar uma tabela chamada orcamento

```
 CREATE TABLE IF NOT EXISTS Orcamento(
	idOrcamento serial PRIMARY KEY,
	produto VARCHAR(90) NOT NULL,
	marca VARCHAR(45) NOT NULL,
	valor MONEY NOT NULL, 
	tipo_instrumento VARCHAR(90) NOT NULL,
	tipo_captadores VARCHAR(20) NOT NULL, 
	modelo VARCHAR(40) NOT NULL, 
	ano int, 
	made_in VARCHAR(15) NOT NULL,
	descricao VARCHAR(200)
);
```

- Checar o orcamento.csv

- Verificar se ele obedece a estrutura de um arquivo csv;

- Observar qual o delimitador usado;

- Em alguns casos é interessante realizar a normalização das tabelas e nisso podem ser acontecer de ter a criação de novas tabelas.

```
COPY Orcamento (produto, marca, valor, tipo_instrumento, tipo_captadores, modelo, ano, made_in, descricao) FROM ‘Local no computador onde está o arquivo\orcamento.csv' DELIMITER ';' CSV HEADER;
```

- Aqui podemos testar para saber se está realmente tudo certo. Que tal realizarmos uma simples consulta?

```
SELECT * FROM Orcamento ;
```

Com tudo certo, agora temos o seu chefe testando você. Ele quer saber o seguinte: produto, marca, valor, tipo_instrumento, modelo, ano, made_in e a descrição da tabela orçamento para o idorcamento = 5.

<h2>Exemplo 2</h2>

A SeVira Solutions, começou a fazer sucesso e agora mais um contrato foi realizado. A Chiquinho HotDogs tem desejando um sistema, para facilitar para os desenvolvedores a equipe de engenharia de requisitos conseguiu com o cliente uma planilha com a lista de preços.

A sua tarefa novamente foi importar um arquivo chamado meulanchinho.csv para um banco de dados do PostgreSQL. 

Então você aceita o desafio?












