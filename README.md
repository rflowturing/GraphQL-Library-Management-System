# GraphQL-Library-Management-System

* *Version*: 1.0.0
* *Authors*: Surya Hendricks, Wolfgang Reip

Description
----
A library management API. 

Technologies
----
*GraphQL*, *NodeJS*, *Express*, *MongoDB*, *JSW*

How to run the projet
----

1. Clone the repository.

2. Launch the terminal from the project's root folder and type **npm run dev**.

3. Navigate to http://localhost:5000/graphql. 

What can you do? 
-----

1. Create a user

```graphql
mutation {
  createUser(name:"jeanne", password:"jean") {
    id
    name  
  }
}
```
2. Login

```graphql
query{
  login(name: "jean", password: "jean") {
    token
  }
}
```
3. Insert the Token in the HTTP **Headers field**

```graphql
{
  "data": {
    "login": {
      "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVlMGEwMmE5ZjIyYTJjNzJiODAxN2Y3ZSIsImlhdCI6MTU3ODQ3Mzk2NCwiZXhwIjoxNTc4NDg1OTY0fQ.cUODwsTLkTMSnza4NAWH3LJ3NTdgGspLKMRhZzixrY4"
    }
  }
}
```
4. Perform queries and mutations such as

```graphql
query{
  books {
    title
    id
  }
}
```
```graphql
mutation{
  createBook(title: "The never ending story", subtitle: "Tome 1"){
    id
    title
  }
}
```








