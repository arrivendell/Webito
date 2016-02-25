## Webito

Project made for ubuntu 13.10 or after, python 2.7
Webito is a simple http-based server api providing user registration, authentication and a feature to make a user able to see its last successful connection timestamps.
No interface design has been done yet so the web interface is really simple.
It is based on Flask, using a mongodb database to persist user data.

To install the dependency packages used in the project run :
```shell
sudo apt-get install python-dev libffi-dev mongodb python-pip
 ```
Then install the virtualenv for python (>=version 14.0.6)
```shell
    pip install virtualenv 
 ```
 
A mongodb instance must be running in order to have the website working accordingly to the requirements.
To launch a mongodb instance listening by default on 127.0.0.1:27017 run :
```shell
sudo mongod --nojournal
 ```
you can run make in the project folder and you will see the virtual environment folders created, to launch the programm then just run, from inside the project web_server folder:
```shell
    ./build/venv/bin/python src/run.py "config.json" 1
 ```


 The configuration file is config.js, it is generated by ruynning config.py.
 In this file you can modify the webserver listenning address.
 
 
 
 Without changing the configuration files, you can access the website on http://0.0.0.0:8080
 From there you can register, login, logout, and display a list of last connections timestamps. Only users with a special role can access this list, but the role is given by default to any new registered user.
 
 To log in as an admin : admin/admin
 Nothing changes except a special page is displayed instead of the normal user connection list page, in case we want to support in the futur special admin features
 
 
 
 

