# 🚀 Challenge 02: Node.js concepts
Made by: [Igor Gois](https://github.com/igorgoiis).

[Documentation in Portuguese.](https://github.com/igorgoiis/desafio-conceitos-node-js/blob/master/README.md)

###	About the challenge

In this challenge I created an application to store repositories in the portfolio that allows the creation, listing, update and removal of the repositories, and in addition allows the repositories to receive "likes".

**Repositories [/repositories]**
- To register a repository **[POST]**

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

- To list all repositories **[GET]**
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
- To update a repository **[PUT]**
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

- To delete a repository **[DELETE]**
	- Response:
		- Status: 204 No Content

**Likes [/repositories/:id/like]**
- To like a repository **[POST]**:
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

## 🏁 Installation
- **Clone the repository:**

	  git clone https://github.com/igorgoiis/bootcamp-desafio-01.git

- **Access the folder:**

	  cd bootcamp-desafio-01

- **Install the dependencies:**

	  yarn

- **Run the server:**

	  yarn dev

	O servidor escuta na porta 3333.

- **Run the tests:**

	  yarn test

Made by: [Igor Gois](https://github.com/igorgoiis).
