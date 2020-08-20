<h1 align="center">🚀 Proffy Server 🚀</h1>

![Badge](/github/logo.png)

<h1 align=center>
  <a href="https://insomnia.rest/run/?label=Proffy%20API&uri=http%3A%2F%2Flocalhost%3A3333%2F" target="_blank"><img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia"></a>
</h1>

<h2>
  👨‍💻 Tecnologias utilizadas
</h2>
<ul>
  <li><h3><a href="https://nodejs.org/pt-br/">NodeJS</a></h3></li>
  <li><h3><a href="https://www.typescriptlang.org/">Typescript</a></h3></li>
  <li><h3><a href="https://expressjs.com/pt-br/">Express</a></h3></li>
  <li><h3><a href="http://knexjs.org/">Knex</a></h3></li>
  <li><h3><a href="https://www.sqlite.org/index.html">Sqlite</a></h3></li>
</ul>

<h2>
  📄 Funcionalidades
</h2>

<ul>
  <h3>Cadastro de professores</h3>
  
  <p><strong>POST: </strong> http://localhost:3333<strong>/classes</strong></p>
  
  ```javascript
  // request body
  {
    "name": "Fulano/a",
    "avatar": "<image_url>",
    "whatsapp": "999669966",
    "bio": "Apaixonado/a em tecnologia!",
    "subject": "Filosofia",
    "cost": 80,
    "schedule": [
      { "week_day": 1, "from": "10:00", "to": "12:00" },
      ...
    ]
  }
  ```

  <strong>Response: status 201</strong>
  
  <h3>Busca de professores</h3>
  
  <p><strong>GET: </strong>http://localhost:3333/classes?<strong>subject=filosofia&week_day=2&time=13:00</strong></p>
  <strong>Response: </strong>

  ```javascript
    [
      {
        "name": "Fulano/a",
        "avatar": "<image_url>",
        "whatsapp": "999669966",
        "bio": "Apaixonado/a em tecnologia",
        "subject": "Filosofia",
        "cost": 80,
        "schedule": [
          { "week_day": 2, "from": "13:00", "to": "14:00" },
          ...
        ]
      },
      ...
    ]
  ```

  <h3>Criar conexões entre alunos e professores</h3>
  
  <p><strong>POST: </strong> http://localhost:3333<strong>/connections</strong></p>

  ```javascript
  // request body
  {
    "user_id": 5,
  }
  ```

  <strong>Response: status 201</strong>

  <h3>Listar quantidade de conexões</h3>
  <p><strong>GET: </strong>http://localhost:3333/<strong>connections</strong></p>

   <strong>Response: </strong>

  ```javascript
    {
      "total": 13
    }
  ```
</ul>

<h2>
  🔍 Requisitos de software
</h2>

<ul>
  <li><h3><a href="https://nodejs.org/pt-br/">NodeJS</a></h3></li>
  <li><h3><a href="https://yarnpkg.com/">Yarn</a></h3></li>
</ul>

<h2>
  💡 Como rodar o projeto?
</h2>

### Clone o repositório para ter uma cópia do código em sua máquina

```bash
$ git clone https://github.com/DeboraZandonai/PROFFY.git 
```

### Navegue até a pasta do projeto

```bash
$ cd PROFFY/server
```

### Carregue as dependências

```bash
$ yarn
```

### Rode o projeto

```bash
$ yarn start
```
<br />

<h4 align=center>Made with ❤️ by <a href="https://www.linkedin.com/in/debora-zandonai-4ab092195/">Debora Zandonai</a></h4>
