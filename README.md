## **API Unity Technical Test**

### **Default data**

The API will have default users and reviews data.  
Some users have reviewed the same game sessions.  
The first two users have not reviewed their corresponding game sessions  
___
### **Data Shape**

* **Users:**
  * number
  * name
  * lastGameSession

* **Reviews:**
  * id
  * rating
  * comments
  * sessionId
  * userId
  * userName
___
### **API Endpoints**

* **GET** `/reviews/:ratingFilter`  
Returns reviews filtered by rating.  
Example: `/reviews/?ratingFilter=5`

* **GET** `/reviews/`  
Return all reviews

* **GET** `/users`  
Returns all users

* **POST** `/reviews/new`  
Creates a new review  
Body payload:
  * rating
  * comments
  * sessionId
  * userId
  * userName  
  
___
### **Running the API Server**

`cd api`  
`npm i`  
`npm start`  


### Usuarios post example:

```

curl -X POST \
  http://localhost:3000/usuarios \
  -H 'Content-Type: application/json' \
  -d '{
    "nome": "Mateus Filipe Schverz",
    "email": "matefs8569@gmail.com",
    "dataNascimento": "2001-02-02",
    "sexo": "masculino",
    "cidade": "Concórdia",
    "estado": "SC",
    "senha": "123",
    "confirmarSenha": "123",
    "cpf": "112.553.389-70",
}'

```