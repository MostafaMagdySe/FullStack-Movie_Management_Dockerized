# FullStack-Movie_Management_Dockerized
This is a Dockerized Version of The Movie Management Website. which means you can easily run the whole project with one line of code. and you just need to Install Docker into your Machine. 

For more inofrmation abot the project, you can visit the backend and the frontend Repos:

Backend:  [Movie-Management BackEnd_repository](https://github.com/MostafaMagdySe/Movie-Management).

FrontEnd  [Movie-Management FrontEnd_repository](https://github.com/MostafaMagdySe/Movie-Management-Front-End).

# Prerequisite
1- You Must install "Docker" into your machine and run it.

2- (optional) if you won't download the project manually and want it to be downloaded automatically, you need to install "Git" software into your machine so that it downloads the project for you.

## Running the Project
Assuming you will download the project via "Git" , if not, you just need to open cmd and navigate to your project's location using "cd" command and head to 3rd line of code directly and run it.

**Steps:**

Open your cmd and run those three lines one by one:

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
and now your project is Running!

## How to use The project

Open your browser and paste this url:
```bash
localhost:4200
```

Now, just use it as you usually use any website by registering your account and then log in.

> [!NOTE]
 >you need to keep your cmd running to have the project running, if you Closed it, and wanted to run the project again, all you have to do is copying and running "line 2 & 3" of code which were provided previously.

## How to Add or Remove Movies
By Default, any created User is considered as a normal User, which can only view the website and change his Information on the  Profile Tab,

to be able to add or remove Movies, you should first gain Access to the Website as an Admin.. you need to do that manually. this prevents unintended Admin Accounts.

to do that.. open another cmd, and paste and run this command:
```bash
docker exec -it postgres-db psql -U postgres -d movies
```
this will allow you to modify the database and changing you Role From a normal user to an admin, and to do that you have to run the next line of code and edit it accordingly to suit your username before running it.

```bash
UPDATE users SET role_id = 1 WHERE username = 'your_user_name';
```
for example if your username was Mostafa, you will have the following line of code:
```bash
UPDATE users SET role_id = 1 WHERE username = 'Mostafa';
```

> [!CAUTION]
>make sure the you changed your_user_name with exactly the same username you used during registeration process to prevent errors.

Once you run this command, feel free to exit the second cmd window which you are currently staying at, log out from your account and log in again.

You will now find new buttons for adding and removing movies. to get more information about that, you can ckeck the backend and front end Repositories' Guides for more information.

Backend:  [Movie-Management BackEnd_repository](https://github.com/MostafaMagdySe/Movie-Management).

FrontEnd  [Movie-Management FrontEnd_repository](https://github.com/MostafaMagdySe/Movie-Management-Front-End).
