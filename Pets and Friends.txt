CREATE DATABASE PETS_FRIEND;
\c pets_friend;

CREATE TABLE COLLAR(
direccion_ip_collar int primary key,
raster VARCHAR (20),
vector VARCHAR (20));
\d COLLAR;

CREATE TABLE MASCOTA(
id_mascota int primary key,
nom_mascota VARCHAR(20),
edad_mascota VARCHAR(20),
color_mascota VARCHAR(20),
raza VARCHAR(20),
peso_mascota int,
sexo_mascota VARCHAR(1));
\d MASCOTA;

CREATE TABLE MONITOREO(
fecha_monitoreo DATE primary key,
hora_monitoreo int);
\d MONITOREO;

CREATE TABLE DUEÑO(
no_ine int primary key, 
nom_dueño varchar(20), 
app_pat_dueño varchar(20), 
app_mat_dueño varchar(20), 
calle varchar(30), 
numero int, 
colonia varchar(30), 
tel_cel_dueño bigint unique,
sexo varchar(1), 
nacionalidad varchar(30), 
edad int);
\d DUEÑO;

INSERT INTO MASCOTA VALUES (011,'HUNTER',1,'BLANCO','PITBULL',11,'M');
INSERT INTO MASCOTA VALUES (012,'KENIA',2,'CAFE','ALASKA',5,'F');
INSERT INTO MASCOTA VALUES (013,'PEPE',7,'BLANCO CON NEGRO','PUG',8,'M');
INSERT INTO MASCOTA VALUES (014,'OSA',2,'GRIS','PITBULL',20,'F');
INSERT INTO MASCOTA VALUES (015,'PELUDO',1,'NEGRO','SALCHICHA',12,'M');
INSERT INTO MASCOTA VALUES (016,'FIRU',7,'BLACO','PITBULL',12,'F');
INSERT INTO MASCOTA VALUES (017,'TACO',2,'CAFE CON BLANCO','PUG',9,'F');
INSERT INTO MASCOTA VALUES (018,'TOTO',3,'CAFE CON BLANCO','PUG',15,'M');
INSERT INTO MASCOTA VALUES (019,'MOLE',3,'NEGRO CON CAFE','PITBULL',13,'M');
INSERT INTO MASCOTA VALUES (020,'MUÑECA',1,'CAFE','CHIHUAHUA',9,'F');

select * from MASCOTA;

INSERT INTO COLLAR VALUES (221,'Normal','Especial');
INSERT INTO COLLAR VALUES (222,'Especial','Especial');
INSERT INTO COLLAR VALUES (223,'Normal','Basico');
INSERT INTO COLLAR VALUES (224,'Normal','Basico');
INSERT INTO COLLAR VALUES (225,'Normal','Riesgo');
INSERT INTO COLLAR VALUES (226,'Especial','Especial');
INSERT INTO COLLAR VALUES (227,'Normal','Basico');
INSERT INTO COLLAR VALUES (228,'Normal','Basico');
INSERT INTO COLLAR VALUES (229,'Normal','Basico');
INSERT INTO COLLAR VALUES (230,'Especial','Riesgo');

select * from COLLAR;

INSERT INTO MONITOREO VALUES ('25-oct-2021','5');
INSERT INTO MONITOREO VALUES ('22-sep-2021','4');
INSERT INTO MONITOREO VALUES ('18-nov-2021','3');
INSERT INTO MONITOREO VALUES ('22-oct-2021','2');
INSERT INTO MONITOREO VALUES ('25-nov-2021','3');
INSERT INTO MONITOREO VALUES ('23-oct-2021','3');
INSERT INTO MONITOREO VALUES ('20-sep-2021','2');
INSERT INTO MONITOREO VALUES ('21-dec-2021','7');
INSERT INTO MONITOREO VALUES ('02-nov-2021','6');
INSERT INTO MONITOREO VALUES ('30-oct-2021','2');

select * from MONITOREO

INSERT INTO DUEÑO VALUES (111,'Luis','Martinez','Lopez','Monarcas',55,'Villa del real','5564732220','M','Mexicano',25);
INSERT INTO DUEÑO VALUES (112,'Maria','Aquino','Montero','Rosa',21,'Ojo de Agua','5534621020','F','Mexicana',22);
INSERT INTO DUEÑO VALUES (113,'Miguel','Lopez','Ontiveros','San marcos',11,'San pablo','5566631968','M','Mexicano',19);
INSERT INTO DUEÑO VALUES (114,'Edric','Sanchez','Martinez','San miguel',12,'Tecamac Centro','5533484073','M','Mexicano',20);
INSERT INTO DUEÑO VALUES (115,'Kevin','Villegaz','Rosales','Monarcas',2,'Villa del real','5532211441','M','Mexicano',22);
INSERT INTO DUEÑO VALUES (116,'Alegadro','Moreno','Leon','Insurgentes',34,'Ecatepec','5518265512','M','Mexicano',18);
INSERT INTO DUEÑO VALUES (117,'Danna','Durante','Arteaga','San Marcos',34,'Villa del real','5598164448','F','Argentina',21);
INSERT INTO DUEÑO VALUES (118,'Fernanda','Durante','Arteaga','San Marcos',34,'Villa del real','5512346912','F','Argentina',29);
INSERT INTO DUEÑO VALUES (119,'Brandon','Martinez','Morales','San Felipe',2,'Villa del real','5571667582','M','Mexicano',19);
INSERT INTO DUEÑO VALUES (120,'Alexis','Vargas','Zarco','5 de mayo',12,'Ecatepec','5519071069','M','Mexicano',22);

select * from DUEÑO;