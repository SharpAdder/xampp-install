### XAMPP instalation for windows 10 | Set system environment variable 

### Installing XAMPP
Downlad XAMPP from here [apache friens](https://www.apachefriends.org/download.html). <br>
I installed version 8.2.0 / PHP 8.2.0 <br>
When installing you will get a warning: Important! Because an activated User Account Control(UAC) on your system some functions of XAMPP are possibly restricted.
With UAC please avoid to install XAMPP to C:\Program Files(missing write permissions). Or deactivate UAC with msconfig after this setup. <br>

Go to start and type in UAC -> get the slider down. Don't worry about this. After the installation go again to start (start button on windows) & type in UAC -> slide back up the slider. <br>
 Continue with the installation. Install XAMPP on your C drive (or on the partition that has the system software installed, in my case is C) <br>
 
 Navigate in the ***xampp*** folder and look for the ***htdocs*** folder. <br>
 ##### All your php projects need to be in the htdocs folder. Path sould look like this: c/xampp/htdocs
 ##### The database you build in mySQL is in the mySQL -> data folder. Path should look like this: xampp/mySQL/data
 When you start XAMPP make sure to start the following: Apache & MySQL servers

#### Running mySQL in the command line/ cmd
1. Open cmd
2. Type in mysq
3. If this message appears: 'mysql' is not recognized as an internal or external command -> set system environment variabile

#### System environment variable
1. Go to start -> tyoe env -> open -> Edid system environment variables -> yes
2. Go to Advanced tb -> select Environment Variables
3. In System Variables -> select Path -> New
4. Variable name = sql | variable value = xampp/mysql/bin   -> press ok
5. back to cmd -> type in mysql -> you should get this error: ERROR 1045 (28000): Access denied for user ....
6. type in: -u root -p & press enter when asked for password
7. you should get this message Welcome to the MariaDB monitor.  Commands end with ; or \g.  
8. Congrats! You are set up to write mysql commands in cmd 😏
