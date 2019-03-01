
# Api Mysql

## Inicio do projeto

Para iniciar esse projeto com dotnet com c# com mysql workbench, abra o prompt de comando(cmd), e va para o Desktop\ com o comando:
```bash
	cd Desktop\
```
E depois criar uma pasta com o comando: (nome de sua pasta no caso agilAPP)
```bash
	mkdir agilAPP 
```
e para entrar o mesmo comando acima de e depois aperte enter:

```bash
	cd agilAPP\
```
apos esse comando vamos para o inicio da criaçao do arquivo dotnet

## Criaçao do dotnet

Apos estar dentro do agilAPP\, digite este comando
```bash
	dotnet new webapi -o agilAPI -n agilAPI
```
a descriçao do comando e, a criaçao do uma nova aplicaçao web o -0 cria a pasta e o -n cria o nome da pasta
 
apos isso entre na pasta 
```bash
	cd agilAPI\
```
e digite o comando:
```bash
	Code .
```
## Execução da aplicação

Para executar a aplicação é necessário abril o MySql workbench.

Primeiramente execute o seguinte comando:


```bash

## String de conexão do banco

# Api Mysql


## Execução da aplicaçã

Primeiramente execute o seguinte comando:

dotnet run
```
Se desejar fechar o container após a execução, digite o comando:

```bash

## String de conexão do banco

Se já possuir um banco de dados MySql e deseja utilizá-lo na aplicação, modifique a string de conexão no arquivo **appsettings.json**, no trecho indicado:

```json
...
"ConnectionStrings": {
    "MySqlDbConnection": "server=localhost;database=NameDatabase;Uid=(Your id in mysql or root);password=(Your password in mysql)"
  },
...

```
