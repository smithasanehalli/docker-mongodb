Run MongoDB in a Docker container, access it from host machine, create table, 
insert data and finally very data.

1. Install Docker
2. Open terminal verify Docker is installed by run cmd                                                                                                                    “$ docker version”
3. To get MongoDB image from docker hub run below cmd, it will download MongoDB software
    $ docker pull mongo (pull latest version) or docker pull mongo:4.0.4 (pull specific version)

4. Deploy the instance on Docker container, mapping ports to access from host 
    $ docker run -d -p 27017-27019:27017-27019 --name mongodb mongo:4.0.4

5.Connect to it using terminal
    $ docker exec -it mongodb bash

6. To launch MongoDB shell client run cmd
    $ mongo

7. To create a database and insert data run 

    show dbs - lists available db

    use students - your db name

    db.students.save({ firstname: “Smith”, lastname: “sanehalli” })
    db.students.save({ firstname: “Amy”, lastname: “guest” })

8.To verify search student from data base
    db.students.find({ firstname: "Nic" })