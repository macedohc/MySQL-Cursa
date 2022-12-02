create database Escola
default character set utf8
default collate utf8_general_ci;

create table alunos (
id int NOT NULL auto_increment,
nome varchar (30) NOT NULL,
nascimento date,
sexo enum ('M','F'),
peso decimal (5,2) ,
altura decimal (3,2) ,
nacionalidade varchar(20) DEFAULT 'Brasil',
PRIMARY KEY (id)
) default charset = utf8;

use escola;

insert into alunos (id, nome, nascimento, sexo, peso, altura, nacionalidade)
values ('1','joan','1998-07-19', 'M' ,'79.9','1.98','Brasil');

insert into alunos (nome, nascimento, sexo, peso, altura, nacionalidade)
values ('joan','1998-07-19', 'M' ,'79.9','1.98','Brasil');

insert into alunos (id, nome, nascimento, sexo, peso, altura, nacionalidade)
values ( default,'joan','1998-07-19', 'M' ,'79.9','1.98', default);

insert into alunos values ( default,'joan','1998-07-19', 'M' ,'79.9','1.98','Brasil');

insert into alunos (id, nome, nascimento, sexo, peso, altura, nacionalidade)
values ('1','Sandra','1998-09-29', 'F' ,'56.9','1.58','EUA'),
('2','Luan','1998-04-12', 'M' ,'79.9','1.98','Brasil'),
('3','Kuan','1998-07-19', 'M' ,'79.9','1.98',default);

select * from alunos;

describe alunos;

alter table alunos
add column endereco varchar (30);

alter table alunos
drop column endereco;

alter table alunos
add column endereco varchar (30) after nascimento;

alter table alunos
add column codigo int first;

alter table alunos
add codigo int first;

alter table alunos
modify column endereco varchar (50);

alter table alunos
modify column endereco varchar (20) not null default '';

alter table alunos 
change column endereco EnderecoPrincipal varchar (40);

alter table alunos
rename to matricula;

create table if not exists cursos (
nome varchar (30) not null unique,
descricao text,
carga int unsigned,
ano year default '2016'
) default charset = utf8;

alter table cursos
add column idcurso int first;

alter table cursos
add primary key (idcurso);

alter table cursos
add column totaulas varchar (5) after carga;

drop table cursos;

drop table if exists cursos;

insert into cursos values
('1','HTML4','Cursos de html5','70','65','2015'),
('2','Jarda','Cursos de java','40','98','2011'),
('3','JavaScript','Cursos de JavaScript','40','25','2014'),
('4','C#','Cursos de html5','70','65','2013'),
('5','Cozinhar','Cursos de comida','50','65','2015'),
('6','Bolo','Como fazer bolo','10','65','2016'),
('7','Dançar','Aula de dança','70','100','2018');

update cursos
set nome = 'HTML5'
where idcurso = '1';

update cursos
set nome = 'Java' , ano = '2014'
where idcurso = '2';

update cursos
set nome = 'Fazer Bolo' , ano = '2014', carga = '30'
where idcurso = '6'
limit 1;

update cursos
set ano = '2012' , carga = '20'
where ano = '2014'; /*Altera todos os dados do banco de dados que
tiverem no ano de 2014, mas para alterar precisa acessar: 
Edit - preferences - sql edit - desmarcar a opção ( safe ... ) 
e depois reconectar no banco de dados*/

update cursos
set ano = '2012' , carga = '20'
where ano = '2014'
limit 3; /*Limitar a quantidade de linhas que tem o
ano de 2014 para alterar para 2012*/

delete from cursos
where idcurso = '7'; /*apaga somente a linha 7*/

delete from cursos
where ano = '2012';
/*apaga todos os dados que tiver no ano de 2012 porém o safe update precisa esta desativado*/

delete from cursos
where ano = '2012'
limit 1; /*apaga somente a linha que tem o ano de 2012, pois esta limitado para 1 linha */

truncate table cursos ; /*apaga todas as linhas*/

select * from cursos;
