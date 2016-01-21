# mongodb
Mongo DB and Spring Boot using RESTful services

# Requirements:
- Java 8
- Gradle
- MongoDB

# Starting up app:
- Start up mongodb
- run ./gradlew bootRun
- to add jvm args, run ./gradlew bootRun -PjvmArgs="-D<key1>=<value1> -D<key2>=<value2>"

# curl commands:
- curl http://localhost:8080
- curl http://localhost:8080/people
- curl -i -X POST -H "Content-Type:application/json" -d '{  "firstName" : "Frodo",  "lastName" : "Baggins" }' http://localhost:8080/people
- curl http://localhost:8080/people/<id>
- curl http://localhost:8080/people/search
- curl http://localhost:8080/people/search/findByLastName?name=Baggins
- curl -X PUT -H "Content-Type:application/json" -d '{ "firstName": "Bilbo", "lastName": "Baggins" }' http://localhost:8080/people/53149b8e3004990b1af9f229
- curl -X PATCH -H "Content-Type:application/json" -d '{ "firstName": "Bilbo Jr." }' http://localhost:8080/people/53149b8e3004990b1af9f229
- curl -X DELETE http://localhost:8080/people/53149b8e3004990b1af9f229

# Mongo DB commands
To have launchd start mongodb at login:
    ln -sfv /usr/local/opt/mongodb/*.plist ~/Library/LaunchAgents
    
Then to load mongodb now:
    launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist

To unload mongodb now:
    launchctl unload ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist

Or, if you don't want/need launchctl, you can just run:
    mongod --config /usr/local/etc/mongod.conf
