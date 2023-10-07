
create database parcial2;
use parcial2;
create table persona(
id_direccion varchar(5) ,
n_calle varchar(10),
colonia varchar(10),
n_casa varchar(10),
n_identidad varchar(10)primary key,
nombre varchar (30),
telefono varchar (10));

create table usuario(
n_seguro varchar (10),
id_empleado varchar(10)primary key,
sueldobase int(10),
horas_trabajo int,
cargo set('profesor','administrativo','servicios'),
nombre varchar(15),
pass set('1','2','3'),
id_usuario varchar(12),
foreign key(id_usuario)references persona(n_identidad));

create table alumno(
horas_semana int,
nombre varchar(30),
descripcion set('ingenieria','artes','administracion'),
id_carrera varchar(10),
id_alumno varchar(10)primary key,
foreign key(id_alumno)references persona(n_identidad));

create table clase(
id varchar(5),
nombre_clase set('ingles','sociales','calculo'),
horas_por_semana set('3','4'),
id_clase varchar(10),
descripcion varchar(30),
foreign key(id)references alumno(id_alumno),
foreign key(id)references usuario(id_empleado));
insert into persona values('223','23','col1','1','1234567890','stevan','tel1');
insert into persona values('224','20','col2','2','1234567891','juan','tel2');
insert into persona values('225','21','col3','3','1234567892','lucas','tel3');
insert into persona values('226','27','col4','4','1234567893','maria','tel4');
insert into persona values('215','29','col5','5','1234567894','stiben','tel5');
insert into persona values('216','12','col6','6','1234567895','isabel','tel6');
insert into persona values('217','15','col7','7','1234567896','rey','tel7');
insert into persona values('218','17','col8','8','1234567897','andres','tel8');
insert into persona values('219','47','col9','9','1234567898','pedro','tel9');
insert into persona values('232','36','col0','0','1234567899','romeo','tel0');


insert into usuario values('01','1230','1300000','8','servicios','stevan','3','1234567890');
insert into usuario values('02','1231','5300000','8','profesor','juan','1','1234567891');
insert into usuario values('03','1232','2800000','8','administrativo','lucas','2','1234567892');
insert into usuario values('04','1233','5800000','8','profesor','maria','1','1234567893');
insert into usuario values('05','1234','1400000','8','servicios','stiben','3','1234567894');
insert into usuario values('06','1235','2600000','8','administrativo','isabel','2','1234567895');
insert into usuario values('07','1236','6500000','8','profesor','rey','1','1234567896');
insert into usuario values('08','1237','2900000','8','administrativo','andres','2','1234567897');
insert into usuario values('09','1238','1500000','8','servicios','pedro','3','1234567898');
insert into usuario values('10','1239','1350000','8','servicios','romeo','3','1234567899');


insert into alumno values ('20','juan','ingenieria','123450','1234567890');
insert into alumno values ('23','lian','artes','123451','1234567891');
insert into alumno values ('22','jose','administracion','123452','1234567892');
insert into alumno values ('21','roberto','ingenieria','123453','1234567893');
insert into alumno values ('20','rosa','artes','123454','1234567894');
insert into alumno values ('23','juana','administracion','123455','1234567895');
insert into alumno values ('19','ana','ingenieria','123456','1234567896');
insert into alumno values ('23','mario','artes','123457','1234567897');
insert into alumno values ('24','lin','administracion','123458','1234567898');
insert into alumno values ('21','luz','ingenieria','123459','1234567899');


insert into clase values('1234567890','ingles','4','1230','lenguas');
insert into clase values('1234567891','sociales','3','1231','etica');
insert into clase values('1234567892','calculo','4','1232','multibariado');
insert into clase values('1234567893','sociales','3','1233','historia');
insert into clase values('1234567894','claculo','4','1234','derivado');
insert into clase values('1234567895','ingles','4','1235','moderno');
insert into clase values('1234567896','sociales','3','1236','historia');
insert into clase values('1234567897','calculo','4','1237','integral');
insert into clase values('1234567898','ingles','4','1238','lenguas');
insert into clase values('1234567899','calculo','4','1239','integral');
