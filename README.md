# OOPS Library System Application

### Tech
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
### Styling and Design
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white)
![Styled Components](https://img.shields.io/badge/styled--components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)
### Testing
![Selenium](https://img.shields.io/badge/-selenium-%43B02A?style=for-the-badge&logo=selenium&logoColor=white)

Welcome to the Library Reservation System! This project provides a simple reservation system for books, movies, and periodicals through user-friendly web interface. Users can browse available items and make reservations online. 

The UI is connected to a Springboot backend and MySql database.
The entire application is contained within the `LibraryCapstone` folder with the UI and backend in separate folders with a binding Dockerfile.

## Setup Instructions
To set up and run the application locally, follow these steps:

    git clone https://github.com/Irenexp/LibraryCapstone.git
    docker-compose up
    
Install dependencies at root of UI directory.

    npm install react-bootstrap bootstrap
    npm install styled-components


## Contributors
Andrew Swinney (@andrewswinney)

Madhavi Swamy (@madhaviswamy)

Shurun Liu (@Irenexp)

Toluwa Adetomiwa (@twg23)

## Run the app

    http://localhost:3030

## Run the tests

    ./run-tests.sh

# REST API

The REST API to the example app is described below.

## Get list of Books

### Request

`@GET`

    curl -XGET -H "Content-type: application/json" 'http://localhost:8080/books'

### Response

   [
    {
        "id": 1,
        "title": "To Kill a Mockingbird",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/to-kill-a-mockingbird.jpg",
        "genre": "FICTION",
        "quantity": 30,
        "available": true
    },
    {
        "id": 2,
        "title": "1984",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/1984.jpg",
        "genre": "FICTION",
        "quantity": 30,
        "available": true
    },
    {
        "id": 3,
        "title": "The Great Gatsby",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/the-great-gatsby.jpg",
        "genre": "ROMANCE",
        "quantity": 30,
        "available": true
    },
    {
        "id": 4,
        "title": "Pride and Prejudice",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/prideandprejudice.jpg",
        "genre": "ACTION",
        "quantity": 30,
        "available": true
    },
    {
        "id": 5,
        "title": "The Hunger Games",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/the-hunger-games.jpg",
        "genre": "SCIENTIFIC",
        "quantity": 30,
        "available": true
    },
    {
        "id": 6,
        "title": "The Da Vinci Code",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/da-vinci-codebook.jpg",
        "genre": "FICTION",
        "quantity": 30,
        "available": true
    },
    {
        "id": 7,
        "title": "The Alchemist",
        "imgUrl": "https://ls-project-books.s3.eu-west-2.amazonaws.com/the-alchemist.jpg",
        "genre": "THRILLER",
        "quantity": 30,
        "available": true
    }
]

## Create a new Thing

### Request

`POST /thing/`

    curl -i -H 'Accept: application/json' -d 'name=Foo&status=new' http://localhost:7000/thing

### Response

    HTTP/1.1 201 Created
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 201 Created
    Connection: close
    Content-Type: application/json
    Location: /thing/1
    Content-Length: 36

    {"id":1,"name":"Foo","status":"new"}
