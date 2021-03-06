# TRABALHO 01:  ATVGen
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo:<br>
Matheus Costa Evangelista: matheus20costa@gmail.com<br>
Natan Paschoal Cypriano: cypriano450@gmail.com<br>
Rafael de Almeida Viana Gusmão: rafaelvgusmao@yahoo.com.br<br>
<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados ATVGen e motivação da escolha realizada. <br>
 
O sistema ATVGen tem como objetivo solucionar problemas de ociosidade que diversas pessoas estão enfrentando durante este período de quarentena. Diante desse cenário de  isolamento social, muitas pessoas tiveram suas principais atividades paralizadas, tais como escolas, faculdades, cursos presenciais, prática de esportes coletivos, trabalho, entre outros. Para melhor aproveitar o tempo ocioso, muitas pessoas começaram a procurar maneiras de ocupar seu tempo livre, buscando cursos para aprendizado, aprendendo novas receitas, fazendo trabalhos artísticos (fanart, escrever, pintar, tirinhas), entre outras atividades.

O objetivo do sistema ATVGen é criar uma comunidade/rede social, na qual pessoas possam encontrar atividades para praticar em seu tempo livre, a partir de outras pessoas que têm gostos semelhantes. O sistema pretende armazenar um grande número de atividades dos mais diversos tipos, desde cursos online até trabalhos artísticos, sendo capaz de recomendar a cada usuário atividades que possam ser do seu interesse. Cada usuário terá a possibilidade de sugerir novas atividades, registrar suas atividades e seguir outros usuários que possuam gostos em comum.<br>


### 3.MINI-MUNDO<br>

O sistema proposto ATVGen conterá as informações aqui detalhadas. Dos usuários, serão armazenados um código identificador, nome, e-mail, telefone, data de nascimento, sexo e senha, além de sua profissão e endereço. Do endereço, são armazenados rua, número, bairro, cidade, estado e CEP. Da profissão, são armazenados código, descrição, nome e nome da empresa. Um usuário pode cadastrar um número indeterminado de cursos, atividades, e trabalhos. Para os cursos, são armazenados código, nome, descrição, carga horária e número de módulos. Para as atividades, armazena-se código, nome, descrição, localização, tipo e data/hora. Com relação aos trabalhos, são armazenados código, nome, descrição, conteúdo, tags e data/hora. Cada trabalho, atividade ou curso deve estar associado a um usuário. Além disso, usuários são capazes de seguir outros usuários, para acompanhar o que eles publicam. Para a funcionalidade seguir, é necessário armazenar o usuário seguindo, o usuário sendo seguido e a data/hora da interação.<br>


### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>

![Alt text](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/images/prototipo.png "Protótipo")<br>
![Arquivo PDF do Protótipo Balsamiq do ATV Gen](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/arquivos/ATVGen.pdf "ATV Gen")
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    
> O sistema ATVGen precisa inicialmente dos seguintes relatórios:
* Relatório das atividades diárias do usuário (exercícios fisicos, passeios, etc...) revelando a descrição, a localização e a data e hora em que as atividades ocorreram.
* Relatório dos trabalhos produzidos pelo usuário (artes, textos, desenhos, musicas, códigos de programação, etc...), contendo uma descrição do trabalho, o conteúdo em si e a data da postagem.
* Relatório dos cursos que o usuário já fez ou está fazendo, o nome do curso, a quantidade de períodos/módulos que ele já cumpriu desse curso e a descrição.
* Relatório que mostre o número de seguidores que esse usuário possui e quem são, revelando seus nomes e foto de perfil.
* Relatório que mostre as informações pessoas do usuario, seu nome, profissão, numero de telefone(opcional), email(opcional) e data de nascimento.
 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    
![Simulação de todos os dados armazenados](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/arquivos/TabelaSistemaATVGen_sample.xlsx?raw=true "Tabela - Sistema ATVGen")
    
    

### 5.MODELO CONCEITUAL<br>
        
![Alt text](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/images/Conceitual.png "Modelo Conceitual")    
        
    
#### 5.1 Validação do Modelo Conceitual
    Auxilio Jurídico: Lucas Neves de Oliveira e  Marlon Santos Macedo
    Segundo a avaliação do grupo, não havia em nenhum erro em nosso modelo conceitual.
     
    Provisões de Emergência: Kelvin Lehrback Guilherme
    Segundo a avaliação do grupo, nhouve incômodo com as entidades atividade e usuário, visto que atividade está vindo da esquerda para a direita, o que aconteceu devido a limitações do BRmodelo para realizar as conexões, e, por isso, foi colocado de cima para baixo, como recomendado pelo professor. Também houve dúvidas com o auto relacionamento do usuário.

#### 5.2 Descrição dos dados 
    USUARIO: Tabela que armazena as informações relativas ao usuário do sistema.
    nome: Campo que armazena o nome de usuário.
    email: Campo que armazena o e-mail do usuário.
    telefone: Campo que armazena o telefone de contato do usuário.
    data_nascimento: Campo que armazena a data de nascimento do usuário.
    senha: Campo que armazena a senha do usuário.
    sexo: Campo que armazena o sexo (M ou F) do usuário.

    ENDERECO: Tabela que armazena as informações relativas ao endereço de um usuário.
    rua: Campo que armazena o nome da rua.
    numero: Campo que armazena o número da residência.
    bairro: Campo que armazena o nome do bairro.
    cidade: Campo que armazena o nome da cidade.
    estado: Campo que armazena o nome do estado.
    cep: Campo que armazena o CEP relacionado ao endereço.

    PROFISSAO: Tabela que armazena as informações relativas à profissão de um usuário.
    nome: Campo que armazena o nome da profissão.
    descricao: Campo que armazena a descrição (informação detalhada) de uma profissão.
    empresa: Campo que armazena o nome da empresa que o usuário trabalha.

    CURSO: Tabela que armazena as informações relativas a um curso cadastrado pelo usuário.
    cod_curso: Campo que armazena o número identificador do curso.
    nome: Campo que armazena o nome do curso cadastrado pelo usuário.
    carga_horaria: Campo que armazena o número de horas para conclusão do curso.
    descricao: Campo que armazena informações detalhadas sobre o curso.
    numero_modulos: Campo que armazena o número de módulos (caso haja) que o curso possui.

    TRABALHO: Tabela que armazena as informações relativas a um trabalho cadastrado pelo usuário.
    cod_trabalho: Campo que armazena o número identificador do trabalho.
    nome: Campo que armazena o nome do trabalho cadastrado pelo usuário.
    descricao: Campo que armazena informações detalhadas sobre o trabalho em questão.
    conteudo: Conteúdo do trabalho, podendo ser texto, imagem, música, vídeo, etc.
    data_hora: Campo que armazena um marcador de data e hora da publicação do trabalho.
    tags: Campo que armazena palavras-chave relacionadas ao trabalho.

    ATIVIDADE: Tabela que armazena as informações relativas a uma atividade realizada pelo usuário.
    cod_atividade: Campo que armazena o número identificador da atividade.
    nome: Campo que armazena o nome da atividade cadastrada pelo usuário.
    descricao: Campo que armazena informações detalhadas sobre a atividade realizada.
    tipo: Campo que armazena o tipo de atividade (física, recreativa, etc.).
    localizacao: Campo que armazena a localização onde a atividade foi realizada.
    data_hora: Campo que armazena um marcador de data e hora da publicação da atividade.

    SEGUIR: Tabela que contém informações sobre interações "seguir" entre os usuários.
    data_hora: Campo que armazena um marcador de data e hora quando aconteceu a interação.


### 6	MODELO LÓGICO<br>
        
![Alt text](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/images/Logico.png "Modelo Lógico")



### 7	MODELO FÍSICO<br>
     
```
create table PROFISSAO (
    codigo serial,
    descricao varchar(240),
    nome varchar(80),
    empresa varchar(80),
    primary key(codigo)
);

create table ENDERECO (
    codigo serial,
    bairro varchar(80),
    numero int,
    cidade varchar(80),
    estado varchar(80),
    cep varchar(9),
    primary key(codigo)
);

create table USUARIO (
    cod_usuario serial,
    nome varchar(50),
    email varchar(80),
    senha varchar(16),
    telefone varchar(15),
    data_nascimento date,
    sexo char(1),
    endereco int, /*chave estrangeira*/
    profissao int, /*chave estrangeira*/
    primary key(cod_usuario)
);

create table SEGUIR (
    codigo serial,
    seguindo int, /*chave estrangeira, esse é o usuário que está sendo seguido (semelhante ao TWITTER e INSTAGRAM)*/
    seguidor int, /*chave estrangeira, esse é o usuário que irá seguir o usuário de cima*/
    data_hora datetime,
    primary key(codigo)
);

create table ATIVIDADE(
    cod_atividade serial,
    data_hora datetime,
    tipo varchar(30),
    nome varchar(50),
    descricao varchar(240),
    localizacao varchar(240),/*Geolocalização*/
    cod_usuario int, /*chave estrangeira*/
    primary key(cod_atividade)
);

create table TRABALHO(
    cod_trabalho serial,
    conteudo varchar(240), /*conteúdo da postagem (foto, video, texto, etc)*/
    data_hora datetime,
    tipo varchar(30),
    nome varchar(50),
    descricao varchar(240),
    cod_usuario int, /*chave estrangeira*/
    primary key(cod_trabalho)
);

create table CURSO(
    cod_curso serial,
    numero_modulos int,
    descricao varchar(240),
    carga_horaria int,
    nome varchar(50),
    cod_usuario int, /*chave estrangeira*/
    primary key(cod_curso)
);
```
        

### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
```
drop table if exists PROFISSAO cascade;
drop table if exists ENDERECO cascade;
drop table if exists USUARIO cascade;
drop table if exists SEGUIR cascade;
drop table if exists ATIVIDADE cascade;
drop table if exists TRABALHO cascade;
drop table if exists CURSO cascade;


/* Criação das tabelas */

create table PROFISSAO (
    codigo serial,
    descricao varchar(240),
    nome varchar(80),
    empresa varchar(80),
    primary key(codigo)
);

create table ENDERECO (
    codigo serial,
    bairro varchar(80),
    numero int,
    cidade varchar(80),
    estado varchar(80),
    cep varchar(9),
    primary key(codigo)
);

create table USUARIO (
    cod_usuario serial,
    nome varchar(50),
    email varchar(80),
    senha varchar(16),
    telefone varchar(15),
    data_nascimento date,
    sexo char(1),
    endereco int, /*chave estrangeira*/
    profissao int, /*chave estrangeira*/
    primary key(cod_usuario)
);

create table SEGUIR (
    codigo serial,
    seguindo int, /* Chave estrangeira, esse é o usuário que está sendo seguido (semelhante ao TWITTER e INSTAGRAM) */
    seguidor int, /* Chave estrangeira, esse é o usuário que irá seguir o usuário de cima */
    data_hora timestamp,
    primary key(codigo)
);

create table ATIVIDADE(
    cod_atividade serial,
    data_hora timestamp,
    tipo varchar(30),
    nome varchar(50),
    descricao varchar(240),
    localizacao varchar(240),/* Geolocalização */
    cod_usuario int, /* Chave estrangeira */
    primary key(cod_atividade)
);

create table TRABALHO(
    cod_trabalho serial,
    conteudo varchar(240), /* Conteúdo da postagem (foto, video, texto, etc) */
    data_hora timestamp,
    tag varchar(30),
    nome varchar(50),
    descricao varchar(240),
    cod_usuario int, /* Chave estrangeira */
    primary key(cod_trabalho)
);

create table CURSO(
    cod_curso serial,
    numero_modulos int,
    descricao varchar(240),
    carga_horaria int,
    nome varchar(50),
    cod_usuario int, /* chave estrangeira */
    primary key(cod_curso)
);

alter table USUARIO add foreign key(profissao) references PROFISSAO(codigo);
alter table USUARIO add foreign key(endereco) references ENDERECO(codigo);
alter table SEGUIR add foreign key(seguidor) references USUARIO(cod_usuario);
alter table SEGUIR add foreign key(seguindo) references USUARIO(cod_usuario);
alter table ATIVIDADE add foreign key(cod_usuario) references USUARIO(cod_usuario);
alter table CURSO add foreign key(cod_usuario) references USUARIO(cod_usuario);
alter table TRABALHO add foreign key(cod_usuario) references USUARIO(cod_usuario);


/* Inserção de dados */

insert into PROFISSAO values

(1, 'Professor da disciplina de Programação Orientada a Objetos.', 'Professor', 'Instituto Federal do Espírito Santo'),
 (2, 'Responsável pelo reparo e manutenção de computadores', 'Técnico em Informática', 'TecnoVix'),
(3, 'Desenvolvedor, atualmente crio aplicativos para celular', 'Programador', 'PicPay'),
(4, 'Pintor e desenhista', 'Designer', 'Desempregado'),
(5, 'Amante de jogos e estudante de gameficação', 'Desnevolvedor', 'SENAI');
                              
insert into ENDERECO values

(1, 'Jacaraípe', 855, 'Serra', 'ES', '15871-325'),
(2, 'Alto da Serra', 434, 'Petrópolis', 'RJ', '16555-701'),
(3, 'Jardim da Penha', 12, 'Vitória', 'ES', '35226-095'),
(4, 'Coqueiral de Itaparica', 1265, 'Vila Velha', 'ES', '13597-951');
                            
insert into USUARIO values

(1, 'Luana Gomes', 'lugomes@gmail.com', 'l1223', '999888776', '1998-11-16', 'F', 2, 2),
(2, 'Marcio Lopes', 'marlopes@gmail.com', 'ml1551', '989884611', '1996-10-06', 'M', 1, 3),
(3, 'Fernando Pires', 'fepires@gmail.com', 'fp03021', '988506123', '1997-04-01', 'M', 4, 4),
(4, 'Marina Dias', 'madias@gmail.com', 'md8246', '971727374', '1999-08-10', 'F', 3, 1);
                            
insert into SEGUIR values

(1, 4, 3, '2020-01-01 00:00:01'),
(2, 3, 1, '2020-09-25 09:45:32'),
(3, 4, 2, '2020-08-24 10:25:12'),
(4, 1, 2, '2020-01-28 11:21:02'),
(5, 3, 2, '2020-11-19 07:01:52'),
(6, 2, 3, '2020-05-09 16:45:39'),
(7, 4, 1, '2020-12-08 19:35:22');
                           
insert into ATIVIDADE values

(1, '2020-04-16', 'Física', 'Corrida', 'Corrida matinal na praia', 'Serra', 1),
(2, '2020-05-13', 'Música', 'Aula de canto', 'Treino para aprimorar o alcance de notas mais agudas', 'Vila Velha', 3),
(3, '2020-06-28', 'Física', 'Treino aeróbico', 'Treino de core com ênfase aprimoramento da capacidade pulmonar', 'Vitória', 4),
(4, '2020-06-30', 'Social', 'Montagem de cestas básicas', 'Montagem de cestas básicas para doação', 'Petrópolis', 2);
                              
insert into TRABALHO values

(1, 'Rosas são vermelhas', '2020-12-08 19:35:22', 'Literatura', 'Meu poema', 'Poema que fiz como passatempo', 1),
(2, 'MyPainting.png', '2020-05-08 16:44:12', 'Arte', 'Pintura de paisagem', 'Pintura feita a partir da vista de minha casa', 2),
(3, 'MyVideo.amv', '2020-09-08 16:44:12', 'Arte', 'Filme amador', 'Compilado de cenas que fiz com auxílio do meu irmão', 4),
(4, 'Artigo sobre redação no ENEM', '2020-08-01 21:40:42', 'Texto', 'Redação ENEM 2020', 'Um exercício de redação que fiz para o ENEM', 3);
                              
insert into CURSO values

(1, 1, 'Noções básicas de lógica de programação', 20, 'Introdução à Lógica de Programação', 1),
(2, 4, 'Programação orientada a objetos avançada, com desenvolvimento de projetos práticos', 60, 'Orientação a Objetos com Java e UML', 1),
(3, 1, 'Aprenda os segredos da respiração e da meditação', 8, 'Meditação para iniciantes', 3),
(4, 2, 'Curso de exercícios para serem praticados em casa apenas com o peso do corpo', 10, 'Como se exercitar em casa?', 4);
```



### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
[Link para o Colab com todos os dados inseridos](https://colab.research.google.com/drive/1goUWH7PVolxr9Br2OW3BNfOHtCw9Irgy?usp=sharing "Colab")

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
    select * from atividade where localizacao = 'Serra';
   ![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_2/92_1.png)
    
    select nome, telefone, data_nascimento from usuario where sexo = 'F';
   ![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_2/92_2.png)
    
    select nome, descricao, carga_horaria, numero_modulos from curso where carga_horaria >= 30;
   ![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_2/92_3.png)
    
    select * from  trabalho where tag = 'Arte';
   ![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_2/92_4.png) 




#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
 
	SELECT * FROM "atividade" where cod_usuario > 1 and tipo = 'Física'
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos1.png "OP_Logicos1")

	SELECT * FROM "atividade" where cod_usuario >= 2 or tipo = 'Física'
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos3.png "OP_Logicos3")

	SELECT * FROM "endereco" where not estado = 'ES'
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos2.png "OP_Logicos2")

	SELECT * FROM "curso" where carga_horaria > 0 and cod_usuario = 1
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos4.png "OP_Logicos4")

	SELECT * FROM "trabalho" where tag = 'Literatura' or tag = 'Texto'
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos5.png "OP_Logicos5")
	
	SELECT carga_horaria*5 as carga_horaria_semanal FROM curso
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos6.png "OP_Logicos6")

	SELECT carga_horaria*5 as carga_horaria_semanal FROM curso 
	SELECT cod_trabalho+1 as cod_trabalho FROM trabalho
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos7.png "OP_Logicos7")

	SELECT numero-1 as numero FROM endereco
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos8.png "OP_Logicos8")
	
	SELECT * FROM "atividade" as ATV
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos9.png "OP_Logicos9")

	SELECT * FROM "atividade" as ATV_Fisicas where tipo='Física'
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos10.png "OP_Logicos10")

	SELECT * FROM "profissao" as Professores where nome = 'Professor' 
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_3/OP_Logicos11.png "OP_Logicos11")

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    
Operadores de Like
    
  	select nome, telefone, data_nascimento from usuario where nome ilike 'm%';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData1.png "LikeEData1")

	select nome, telefone, data_nascimento from usuario where telefone like '%4';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData2.png "LikeEData2")

	select nome, descricao, carga_horaria, numero_modulos from curso where nome not like '%exercitar%';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData3.png "LikeEData3")

	select nome, conteudo, tag, descricao from trabalho where descricao like '%p_';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData4.png "LikeEData4")

	select * from atividade where localizacao not like '_i%';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData5.png "LikeEData5")
    
Operadores de DATAS
    
    select nome, email, data_nascimento, date_part('year', (age(current_date, data_nascimento))) as idade from usuario;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData6.png "LikeEData6")

	select nome, current_date - (data_hora) as tempo_de_publicação from trabalho;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData7.png "LikeEData7")

	select nome, current_date - (data_hora) as tempo_de_publicação from atividade;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData8.png "LikeEData8")

	select nome, extract('month' from data_hora) as mes_de_publicacao from atividade;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData9.png "LikeEData9")

	select nome, date_part('month', data_nascimento) as mes_de_aniversario from usuario;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData10.png "LikeEData10")

	select now(), data_hora as data_da_publicação from atividade;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData11.png "LikeEData11")

	select nome, conteudo, data_hora, tag, descricao from trabalho t2 where conteudo ilike 'm%';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_4/LikeEData12.png "LikeEData12")

OBS: não foi possivel usar o current_time pois os formatos de nenhuma data armazenada no banco tem compatibilidade 

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>

	start transaction;

	update profissao set nome = 'Chef' where nome = 'Cozinheiro';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_5/Update1.png "Update1")

	update endereco set numero = 374 where bairro = 'Alto da Serra';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_5/Update2.png "Update2")

	update atividade set tipo = 'Aeróbica' where cod_atividade = 1;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_5/Update3.png "Update3")

	delete from profissao where codigo > 6;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_5/Delete1.png "Delete1")

	delete from endereco where estado = 'RS';
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_5/Delete2.png "Delete2")

	delete from atividade where cod_usuario = 4;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_5/Delete3.png "Delete3")

	commit;


#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>

	select * from usuario 
	inner join endereco on endereco.codigo = usuario.endereco 
	inner join profissao on profissao.codigo = usuario.profissao 
	inner join seguir on usuario.cod_usuario = seguir.seguindo 
	inner join usuario u on u.cod_usuario = seguir.seguidor 
	inner join atividade on atividade.cod_usuario = usuario.cod_usuario
	inner join curso on curso.cod_usuario = usuario.cod_usuario
      	inner join trabalho on trabalho.cod_usuario = usuario.cod_usuario;
	
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_6/96-1.png)
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_6/96-2.png)
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_6/96-3.png)

 
#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

	select e.estado, count(e.estado) as qtd_usuarios from endereco e group by e.estado order by qtd_usuarios desc
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_7/97_1.png)

	select tipo, count(tipo) from atividade group by tipo order by count(tipo) desc
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_7/97_2.png)

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
   	SELECT * FROM usuario a full join atividade b on a.cod_usuario = b.cod_usuario
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_8/98_1.png)
	
	SELECT * FROM usuario a left outer join curso b on a.cod_usuario = b.cod_usuario
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_8/98_2.png)

	SELECT * FROM endereco right outer join usuario on codigo = cod_usuario
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_8/98_3.png)

	SELECT * FROM usuario a full outer join trabalho b on a.cod_usuario = b.cod_usuario
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_8/98_4.png)

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>

SELF JOIN
     
OBS: Em nenhum momento em nosso projeto há um relacionamento de uma tabela com ela mesma sem haver um intermediário. 
O mais próximo que temos de um self join é a relação Usuario-Seguir-Usuario. 
A tabela seguir no modelo conceitual é uma relação, caso possa ser tratada como self join ficaria da seguinte forma

Esse select irá retornar quem são os seguidores de cada usuário

   	select usuario.nome, u.nome from usuario 
	inner join seguir on seguir.seguindo = usuario.cod_usuario 
	inner join usuario u on u.cod_usuario = seguir.seguidor;


Esse select irá retornar quantos seguidores os usuário tem

   	select usuario.nome, count(u.nome) from usuario 
	inner join seguir on seguir.seguindo = usuario.cod_usuario 
	inner join usuario u on u.cod_usuario = seguir.seguidor group by usuario.nome;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/99_1-99_2.png)
		
VIEW
    
    create view Dados_Pessoais as
	select usuario.nome as nome_usuario, usuario.email, usuario.telefone, 
		usuario.sexo, usuario.data_nascimento, endereco.cep, endereco.estado,
		endereco.cidade, endereco.bairro, endereco.numero, profissao.nome as profissao, profissao.empresa, profissao.descricao from usuario 
		inner join endereco on endereco.codigo = usuario.endereco 
		inner join profissao on profissao.codigo = usuario.profissao;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_1.png)
		
    create view Quem_Estou_Seguindo as
	select usuario.nome as usuario, u.nome as seguindo from usuario 
		inner join seguir on seguir.seguidor = usuario.cod_usuario 
		inner join usuario u on u.cod_usuario = seguir.seguindo order by usuario.nome;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_2.png)
		
    create view Quem_Esta_Me_Seguindo as
	select usuario.nome as usuario, u.nome as seguidor from usuario 
		inner join seguir on seguir.seguindo = usuario.cod_usuario 
		inner join usuario u on u.cod_usuario = seguir.seguidor order by usuario.nome;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_3.png)
		
    create view Trabalhos_do_Usuario as
	select usuario.nome as autor, usuario.email, trabalho.nome as obra, 
		trabalho.descricao, trabalho.tag, trabalho.conteudo from usuario
		inner join trabalho on trabalho.cod_usuario = usuario.cod_usuario;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_4.png)
		
    create view Atividades_do_Usuario as
	select usuario.nome as autor, usuario.email, atividade.nome as atividade, 
		atividade.descricao, atividade.tipo, atividade.localizacao from usuario
		inner join atividade on atividade.cod_usuario = usuario.cod_usuario;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_5.png)
		
    create view Cursos_do_Usuario as
	select usuario.nome as aluno, usuario.email, curso.nome as curso, 
		curso.descricao, curso.carga_horaria , curso.numero_modulos from usuario
		inner join curso on curso.cod_usuario = usuario.cod_usuario;
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_6.png)
		
    create view Quantidade_de_trabalhos_por_mes as
	select usuario.nome, count(trabalho.nome) as quantidade, extract(month from trabalho.data_hora) as mes, extract(year from trabalho.data_hora) as ano from usuario 
		inner join trabalho on trabalho.cod_usuario = usuario.cod_usuario
		group by usuario.nome, extract(month from trabalho.data_hora), extract(year from trabalho.data_hora);
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_7.png)
		
    create view Quantidade_de_atividades_por_mes as	
	select usuario.nome, count(atividade.nome) as quantidade, extract(month from atividade.data_hora) as mes, extract(year from atividade.data_hora) as ano from usuario 
		inner join atividade on atividade.cod_usuario = usuario.cod_usuario
		group by usuario.nome, extract(month from atividade.data_hora), extract(year from atividade.data_hora);
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_9/View_99_8.png)
    

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
    	SELECT nome FROM curso where numero_modulos in (2,4)
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_10/910_1.png)


	SELECT * FROM curso where carga_horaria > (select avg(carga_horaria) from curso)
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_10/910_2.png)

	SELECT cod_usuario, usuario.nome, count(*) as qtd_pessoas_seguindo 
	FROM seguir inner join usuario on usuario.cod_usuario = seguir.seguindo
	where seguindo in (1,6) group by cod_usuario, usuario.nome
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_10/910_3.png)

	select * from trabalho where tag in (select distinct tag from trabalho where tag<>'Arte'
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Consultas/9_10/910_4.png)

	
[Link para o Colab com todas as consultas em tempo real](https://colab.research.google.com/drive/1goUWH7PVolxr9Br2OW3BNfOHtCw9Irgy?usp=sharing "Colab")

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### Relatório 1
#### Objetivo: Obter relatório que mostre os cinco perfis com mais seguidores da rede social
##### Código para obtenção do resultado:
	
	select usuario.nome, count(u.nome) as numero_seguidores 
               from usuario inner join seguir on seguir.seguindo = usuario.cod_usuario 
               inner join usuario u on u.cod_usuario = seguir.seguidor group by usuario.nome;
	       
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%201/Tabela.png "tabela 1")

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%201/relatorio.png "relatorio 1")

	Pode-se reparar que no momento em que análise foi feita, o usuario com maior numero de seguidores era a Marina Dias.
	
	
#### Relatório 2
#### Objetivo: Obter relatório que mostre o número de usuários da rede social por estado
##### Código para obtenção do resultado:

	select e.estado, count(e.estado) as quantidade_usuarios from endereco e 
	group by e.estado order by quantidade_usuarios desc
		
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%202/tabela.png "tabela 2")

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%202/relatorio.png "relatorio 2")

	Pode-se observar que no momento em que a análise foi feita, o estado em que a rede social mais deu certo foi no Espírito Santo.
	
	

#### Relatório 3
#### Objetivo: Obter relatório que mostre a quantidade de Atividades postadas em cada mês, acumulado de todos os anos.
##### Código para obtenção do resultado:
	select count(atividade.nome) as quantidade_atividade, extract(month from atividade.data_hora) as mes from usuario 
	inner join atividade on atividade.cod_usuario = usuario.cod_usuario
	group by  extract(month from atividade.data_hora) order by extract(month from atividade.data_hora);

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%203/1.png)

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%203/2.png)
	
	Pode-se observar que no momento da análise, o mês de maio foi o de maior número de atividades, enquanto o meses de fevereiro e março não tiveram atividades.
	
#### Relatório 4
#### Objetivo: Obter relatório que retorne as tags mais utilizadas quando um usuário posta um trabalho.
##### Código para obtenção do resultado:
	SELECT tag,count(*) as quantidade_trabalho FROM trabalho group by tag order by tag
	
![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%204/1.png)

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%204/2.png)

	Pode-se observar que no momento da análise, as tags Arte e Aula empataram com o maior número de trabalhos
	
#### Relatório 5
#### Objetivo: Obter relatório que retorne a quantidade de cursos cadastrados por cada usuário
##### Código para obtenção do resultado:
	select usuario.nome as aluno, count(curso.nome) as quantidade_curso 
	from usuario inner join curso on curso.cod_usuario = usuario.cod_usuario group by usuario.nome order by usuario.nome;

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%205/1.png)

![Alt text](https://github.com/rafael-gusmao/TrabalhoBD-ATVGen/blob/master/images/Relatorio/Relatorio%205/2.png)

	Neste relatório, vemos que a média de cursos por pessoa é de aproximadamente 1.5 

#### Observação: É importante lembrar que, por se tratar de uma rede social, os  relatórios podem acabar sendo muito semelhantes. Para não acontecerem relatórios repetitivos, optamos por fazer um gráfico diferente para cada tipo de postagem do usuário (Trabalho, Atividade e Curso), mas basicamente o mesmo relatório que foi gerado para descobrir o número de atividades postadas no mês (Relatório 3), serve também para a tabela curso e trabalho. O mesmo vale para o Relatório 5.


### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


