
# Api Mysql
## Ferramentas necessarias
```bash
	->Visual studio code
	->Mysql workbench
	->MysqlConnector
```
## Conhecimentos Necessarios
```bash
	1-Logica de programaçao
	2-C# estruturado
	3-C# orintado a objetos
	4-ASP.net 
	5-HTML/CSS 
	6-SQL language
```
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
apos isso o visual studio code ira abrir, senao abrir ou comando nao for reconhecido apenas abra a pasta pelo proprio vs code
## Extensões necessarias no vs code
 ```bash
	vscode-database
	c#
	c# extensions
	Material icon Theme
	NuGet Packge Maneger
	TSlint
	Path Intellisense
	Bracket Pair Colorizer
```

## Configuraçao da aplicaçao

No vscode voce ira no arquivo startup.cs e ira comentar as seguintes linhas:
```bash
	 app.UseHsts();
	 app.UseHttpsRedirection();
```
Seguindo a linha de modificaçoes crie duas pastas dentro do agilAPI: Data e Models

Apos criar a pasta Models crie uma nova classe em c# chamada Person
e detro desta classe ira encapsular estar tres variaveis 

```bash
	public int Id { get; set; }
        public string tbName { get; set; }
        public string tbIndex { get; set; }
```	
Logo A pasta data ira criar a classe DataContext:

```bash
	public class DataContext : DbContext{ // herança da classe DbContext e ira importar o Microsoft.EntityFrameworkCore;
    
        public DataContext(DbContextOptions<DataContext> options) :base(options){} // construtor da classe com O DbContextOptions<DataContext>-- uma lista de dados, passando por parametro uma variavel chamada options

        public DbSet<Person> Persons{get; set;}// Uma lista encapsulada de pessoas sendo setadas pelo banco e dados;
    }
```
## Sql
 Criar um banco de dados chamado agilAPP, mas nao preencher ou criar tabelas pois o Entity Framework ira fazer isso sozinho;

## Configuraçao do .json

Entre no arquivo appsettings.json e acima do logging crie issp
```bash
	"ConnectionStrings":{
  	"MySqlDbConnection": "Server=localhost;Database=agilAPP;Uid=root;password=toort@"
  	},
```	
## Configurando o Startup.cs

  abra o terminal do vscode e digite este comando
  ```bash
  	dotnet add package MySql.Data.EntityFramework
  ```
  espere instalar e Digite o comando ctrl+p e digite >NuGet Packge Maneger: Add Package, tecle enter,
  apos isso digite o comando MySql.Data.EntityFramworkCore
  enter novamente e selecione a versao so seu myql
 
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
