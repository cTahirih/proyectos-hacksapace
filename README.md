# HackSpace

Como parte de mi formación en este informe resumo lo que logré aprender de manera autodidacta con ayuda de la comunidad de HackSpace.
Mi aprendizaje lo orienté al lado backend con NodeJS por lo que empecé construyendo a medida que aprendía mis primeras API Rest con node y dandome soporte
con MongoDB como base de datos, mis resultados están en el siguiente [repositorio](https://github.com/cTahirih/CRUD-app-node).
Como proyecto final realicé un chat usando Sockets, mySQL, NodeJS y React de lado frontend el [frontend](https://github.com/cTahirih/app-msg-front) y el backend en este [repositorio](https://github.com/cTahirih/app-msg)
El proyecto tiene las siguientes pantallas:
![image](https://user-images.githubusercontent.com/32286691/121935605-3c4f5380-cd0e-11eb-9f9b-3d9dd2125138.png)
![image](https://user-images.githubusercontent.com/32286691/121935659-496c4280-cd0e-11eb-81ee-09dde6766b53.png)
![image](https://user-images.githubusercontent.com/32286691/121935578-322d5500-cd0e-11eb-9b1d-5a530c9f4390.png)
El script para la base de datos es el siguiente:
```
create database appmessenger;
use appmessenger;

create table user(
user_id int not null auto_increment,
user_name varchar(500) not null,
user_lastname varchar(500) not null,
user_email varchar(500) not null UNIQUE,
user_password varchar(500) not null,
user_avatar varchar(45) not null,
constraint user_pk primary key (user_id));

create table message (
message_id int(11) not null auto_increment,
message_body varchar(500) null,
message_id_user int not null,
message_date datetime not null,
constraint message_pk primary key (message_id),
constraint message_user foreign key (message_id_user) references user (user_id));
```
