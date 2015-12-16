# mongodb
Mongo DB and Spring Boot

Requirements:
- Java 8
- Gradle
- MongoDB

Starting up app:
- Start up mongodb
- run gradle bootRun

curl commands:
$ curl http://localhost:8080
$ curl http://localhost:8080/people
$ curl -i -X POST -H "Content-Type:application/json" -d '{  "firstName" : "Frodo",  "lastName" : "Baggins" }' http://localhost:8080/people
$ curl http://localhost:8080/people/<id>
$ curl http://localhost:8080/people/search
$ curl http://localhost:8080/people/search/findByLastName?name=Baggins
$ curl -X PUT -H "Content-Type:application/json" -d '{ "firstName": "Bilbo", "lastName": "Baggins" }' http://localhost:8080/people/53149b8e3004990b1af9f229
$ curl -X PATCH -H "Content-Type:application/json" -d '{ "firstName": "Bilbo Jr." }' http://localhost:8080/people/53149b8e3004990b1af9f229
$ curl -X DELETE http://localhost:8080/people/53149b8e3004990b1af9f229
