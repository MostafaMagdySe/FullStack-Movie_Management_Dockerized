# FullStack-Movie_Management_Dockerized
This a Dockerized Version of The Movie Management Website. which means you can easily run the whole project with one line of code. and you just need to Install Docker to your Machine.

#Prerequisite
You just need to install Docker and git on your machine And you are ready!

##Running the Project
open your cmd and run those three lines one by one:
1st Line:
```bash
git clone --recursive https://github.com/MostafaMagdySe/FullStack-Movie_Management_Dockerized.git
```
2nd Line:
```bash
cd FullStack-Movie_Management_Dockerized
```
3rd Line:
```bash
docker-compose up --build
```
and now your project is Running.

##How to use The project

open your browser and paste this url:
```bash
localhost:4200
```

now, just use it as a normal website by registering

note: you need to keep your cmd running to have the project running, if you Closed it, and wanted to run the project again, all you have to do is using cd to go to go to your project's folder.. and run "docker-compose up" in your cmd.

##How to Add or Remove Movies
By Default, any created User is considered as a normal User, which can only view the website and change his Information on Profile Tab,
to be able to add or remove Movies, you should first gain Access to the Website as an Admin.. you need to do that manually. this prevents unintended Admin Accounts.

to do that.. open another cmd, and paste and run this command:
```bash
docker exec -it postgres-db psql -U postgres -d movies
```
this will allow you to modidy the database and changing you Role From a normal user to an admin, and to do that you have to edit the next line of code accordingly to suit your username 
```bash
UPDATE users SET role_id = 1 WHERE username = 'your_user_name';
```
in the previous line of code, make sure the you changed your_user_name with the username you used during registeration process.

Once you run this command, feel free to exist the second cmd window which you are currently staying at, log out from your account and log in again, and you will find new buttons for adding and removing movies. to get more information about that, you can ckeck the backend and front end Repositories for more information
Backend:  [Movie-Management BackEnd_repository](https://github.com/MostafaMagdySe/Movie-Management).
FrontEnd  [Movie-Management FrontEnd_repository](https://github.com/MostafaMagdySe/Movie-Management-Front-End).
