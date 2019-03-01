
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
	cd agilAPP
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
