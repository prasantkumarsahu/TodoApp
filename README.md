# Todo App
This is a API project for insert, read, update, and delete Todos.

![Spring Boot](https://img.shields.io/badge/Spring_Boot-F2F4F9?style=for-the-badge&logo=spring-boot "Spring Boot") ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white "Java") ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white "Postman") ![Google Chrome](https://img.shields.io/badge/Google%20Chrome-4285F4?style=for-the-badge&logo=GoogleChrome&logoColor=white "Google Chrome")

## Frameworks and Languages
![Java v17](https://img.shields.io/badge/Java-v17-green "Java 17") ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-v3.0.5-brightgreen "Spring Boot v3.0.5")

---
## Browser / Tools
![Google Chrome](https://img.shields.io/badge/Google%20Chrome-v112.0.5615.138-yellow "Google Chrome") ![Postman](https://img.shields.io/badge/Postman-v10.13.0-orange "Postman")
---

## Model
- ### Todo
    - ```java
      private String id;
      ```
    - ```java
      private String todoName;
      ```
    - ```java
      private boolean todoStatus;
      ```
## Dataflow
- ### End Points / Controllers
    - `@GetMapping(value = "/getAllTodos")`
    - `@GetMapping(value = "/getTodosByStatus")`
    - `@RequestMapping(value = "/getTodoById/{id}",method = RequestMethod.GET)`
    - `@PostMapping(value = "/addTodo")`
    - `@DeleteMapping(value = "/deleteTodoById/{id}")`
    - `@PutMapping(value = "/updateTodoById/{id}/{status}")`
- ### Services
    - ```java
        public List<Todo> getAllTodos()
      ```
    - ```java
        public String addMyTodo(Todo todo)
      ```
    - ```java
        public List<Todo> getTodosByUserStatus(String status)
        ```
    - ```java
        public Todo getTodoBasedOnId(String id)
        ```
    - ```java
        public String removeTodoById(String id)
        ```
    - ```java
        public String updateTodoStatusById(String id,String status)
      ```
- ### Repository
    - ```java
       public List<Todo> getTodosFromDataSource()
      ```
    - ```java
        public boolean remove(Todo todo)
      ```
    - ```java
        public boolean update(String id, boolean status)
      ```
    - ```java
        public boolean save(Todo todo)
      ```
- ### Database
    I haven't used any **Database** in this project yet. But for data storing I have used a `Collection`.

    ```java
    private List<Todo> todoList
    ```
---
## Datastructures
- `ArrayList<>`
---
## Summary
This API is a `Spring Boot` project that is about managing Todos. We can create, read, update, and delete Todos. In this project request is sent from the client on HTTP in JSON body or from path variable and stored in object then response is sent back from the server by JSON format to the client.

