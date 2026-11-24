# Diagrama de clases UML — Flaskr

Este documento tiene como objetivo documentar el diagrama de clases UML del modelo de datos de la aplicación Flaskr (`User` y `Post`), mostrando sus atributos, métodos y relación 1:N.

```mermaid
classDiagram
    class User {
        -int id
        -string username
        -string password
        +register()
        +login()
        +logout()
    }

    class Post {
        -int id
        -int author_id
        -timestamp created
        -string title
        -string body
        +create()
        +update()
        +delete()
    }

    User "1" --> "0..*" Post : crea
```