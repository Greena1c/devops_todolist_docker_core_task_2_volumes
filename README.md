#### Requirements
1. Prepare a Dockerfile to run a MySQL database, based on official MySQL Image, name file Dockerfile.mysql
2. Dockerfile should contain ENV variables to initialize app_db database
3. Dockerfile should contain ENV variables to initialize app_user with password 1234
4. Build mysql image with a name and tag mysql-local:1.0.0
5. You should be able successfully run a container with MySQL with a Volumes Attached
6. Push mysql-local:1.0.0 to your personal docker hub into mysql-local repository
7. Run mysql-local:1.0.0 onn your machine
8. Update the python app db config with an IP of a running MySQL server container (without it, the app container won’t build)
9. Build and run your updated app
10. Take a screenshot of a terminal with successfully started application
11. Push Image with a name and tag: todoapp:2.0.0 to yout Docker Hub repository
12. Update README.md with instructions on how to run MySQL container with a volume attached
13. Update README.md with instructions on how to run an App container which will connect to a MySQL db container.
14. README.md should contain a link to your personal docker hub repository win an app image
15. README.md should contain instructions on how to access the application via a browser.
16. Create PR with your changes and attach it for validation on a platform



## 12
docker run -d -p 3306:3306 --name mysql-container -v mysql-data:/var/lib/mysql mysql-local:1.0.0
## 13
docker run -d -p 8080:8080 --name todoapp-container --link mysql-container:mysql todoapp:2.0.0
## 14
https://hub.docker.com/r/greena1c/mysql-local
https://hub.docker.com/r/greena1c/todoapp

## 15
http://localhost:8080/