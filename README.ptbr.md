# 🚀 Desafio 02: Conceitos do Node.js
Feito por: [Igor Gois](https://github.com/igorgoiis).

###	Sobre o desafio
Neste desafio criei uma aplicação para armazenar repositórios do portfólio que permite a criação, listagem atualização e remoção dos repositórios,e além disso permite que os repositórios possam receber "likes".

**Repositories [/repositories]**
- Para cadastrar um repositório **[POST]**

	 - Request:

			{
				"title": "Desafio Node.js",
				"url": "http://github.com/test",
				"techs": [
					"Node.js", 
					"test"
				]
			}
	- Response:		

			{
				"id": "ffa8b7a8-42bb-4e1c-bffd-e28084c3ef8f",
				"title": "Desafio Node.js",
				"url": "http://github.com/test",
				"techs": [
					 "Node.js",
					 "test"
				],
				"likes": 0
			}

- Para listar todos os repositórios **[GET]**
	- Response:
		

		  [
			  {
				  "id": "ffa8b7a8-42bb-4e1c-bffd-e28084c3ef8f",
			    "title": "Desafio Node.js",
			    "url": "http://github.com/test",
			    "techs": [
				     "Node.js",
				     "test"
			    ],
			    "likes": 0
			  },
			  {
			    "id": "6bcba21f-a983-40b9-96fd-526ea20b6835",
			    "title": "Desafio Node.js 2",
			    "url": "http://github.com/test...",
			    "techs": [
			      "Node.js",
			      "test"
			    ],
			    "likes": 0
			  }
		  ]

**Repositories [/repositories/:id]**
- Para atualizar um repositório **[PUT]**
	- Request:
		

		  {
			  "title": "Desafio Node.js Concluido",
		      "url": "http://github.com/concluido",
		      "techs": [
			      "Node.js",
			      "Insomnia"
			  ]
		  }
	- Response:
				

		  {
			  "id": "6bcba21f-a983-40b9-96fd-526ea20b6835",
		      "title": "Desafio Node.js Concluido",
		      "url": "http://github.com/concluido",
		      "techs": [
			      "Node.js",
			      "Insomnia"
			  ],
				"likes": 0
		  }
- Para deletar um repositório **[DELETE]**
	- Response:
		- Status: 204 No Content

**Likes [/repositories/:id/like]**
- Para dar like em um repositório **[POST]**:
	- Response:
		

		    {
			    "id": "ffa8b7a8-42bb-4e1c-bffd-e28084c3ef8f",
		    	"title": "Desafio Node.js",
		    	"url": "http://github.com/test",
		    	"techs": [
			    	"Node.js",
		    		"test"
		    	],
		    	"likes": 1
		    }

## 🏁 Instalação
- **Clone o repositório:**

	  git clone https://github.com/igorgoiis/bootcamp-desafio-01.git

- **Acesse a pasta:**

	  cd bootcamp-desafio-01

- **Instale as dependências:**

	  yarn

- **Execute o servidor:**

	  yarn dev

	O servidor escuta na porta 3333.

- **Execute os testes:**

	  yarn test

Feito por: [Igor Gois](https://github.com/igorgoiis).
