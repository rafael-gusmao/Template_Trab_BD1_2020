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
 
O sistema ATVGen tem como objetivo solucionar problemas de ociosidade que muitas pessoas estão enfrentando durante este período de quarentena. Diante desse cenário de  isolamento social, muitas pessoas tiveram suas principais atividades paralizadas, tais como escolas, faculdades, cursos presenciais, prática de esportes coletivos, trabalho, entre outros. Para melhor aproveitar o tempo ocioso, muitas pessoas começaram a procurar maneiras de ocupar seu tempo livre, buscando cursos para aprendizado, aprendendo novas receitas, fazendo trabalhos artísticos (fanart, escrever, pintar, tirinhas), entre outras atividades.

O objetivo do sistema ATVGen é criar uma comunidade/rede social, na qual pessoas possam encontrar atividades para praticar em seu tempo livre, a partir de outras pessoas que têm gostos semelhantes. O sistema pretende armazenar um grande número de atividades dos mais diversos tipos, desde cursos online até trabalhos artísticos, sendo capaz de recomendar a cada usuário atividades que possam ser do seu interesse. Cada usuário terá a possibilidade de sugerir novas atividades, registrar suas atividades e seguir outros usuários que sejam do seu interesse.<br>
 

### 3.MINI-MUNDO<br>

O sistema proposto ATVGen conterá as informações aqui detalhadas. Dos usuários, serão armazenados um código identificador, nome, e-mail, telefone, data de nascimento, sexo e senha, além de sua profissão e endereço. Do endereço, são armazenados rua, número, bairro, cidade, estado e CEP. Da profissão, são armazenados código, descrição, nome e nome da empresa. Um usuário pode cadastrar um número indeterminado de cursos, atividades, e trabalhos. Para os cursos, são armazenados código, nome, descrição, carga horária e número de módulos. Para as atividades, armazena-se código, nome, descrição, localização, tipo e data/hora. Com relação aos trabalhos, são armazenados código, nome, descrição, conteúdo, tags e data/hora. Cada trabalho, atividade ou curso deve estar associado a um usuário. Além disso, usuários são capazes de seguir outros usuários, para acompanhar o que eles publicam. Para a funcionalidade seguir, é necessário armazenar o usuário seguindo, o usuário sendo seguido e a data/hora da interação.<br>


### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>

![Arquivo PDF do Protótipo Balsamiq do ATV Gen](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/ATVGen.pdf "ATV Gen")
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    
> O sistem ATVGen precisa inicialmente dos seguintes relatórios:
* Relatório com as atividades diarias do usuario (exercicios fisicos, passeios, etc...) revelando a descrição, a localização e a data em que atividade ocorreu.
* Relatório com os trabalhos produzidos pelo usuario (artes, textos, desenhos, musicas, codigos programação, etc...) em que conterá uma descrição do trabalho, o coteudo em si e a data da postagem.
* Relatorio que mostre os cursos que o usuario ja fez ou esta fazendo, o nome do curso, a quantidade de periodos que ele ja fez desse curso e a descrição.
* Relatório que mostre as opiniões do usuario sobre determinado curso que o usuario ja fez ou esta fazendo. 
* Relatório que mostre o numero de seguidores que esse usuario possue e quem são eles, revelando seus nomes e foto de perfil.

 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/images/Conceitual.png "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
        
![Alt text](https://github.com/rafael-gusmao/Template_Trab_BD1_2020/blob/master/images/Logico.png "Modelo Lógico")



### 7	MODELO FÍSICO<br>
     
```
create database ATVGEN;
use ATVGEN;

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
    seguindo int, /*chave estrangeira, esse Ã© o usuario que esta sendo seguido (semelhante ao TWITTER e INSTAGRAM)*/
    seguidor int, /*chave estrangeira, esse Ã© o usuario que irÃ¡ seguir o usuario de cima*/
    data_hora datetime,
    primary key(codigo)
);

create table ATIVIDADE(
	cod_atividade serial,
    data_hora datetime,
    tipo varchar(30),
    nome varchar(50),
    descricao varchar(240),
    localizacao varchar(240),/*GeolocalizaÃ§Ã£o*/
    cod_usuario int, /*chave estrangeira*/
    primary key(cod_atividade)
);

create table TRABALHO(
	cod_trabalho serial,
    conteudo varchar(240), /*coteudo da postagem (foto, video, texto, etc)*/
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

/* Criação do banco de dados */

create database ATVGEN;
use ATVGEN;

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
    seguindo int, /*chave estrangeira, esse é o usuario que esta sendo seguido (semelhante ao TWITTER e INSTAGRAM)*/
    seguidor int, /*chave estrangeira, esse é o usuario que irá seguir o usuario de cima*/
    data_hora timestamp,
    primary key(codigo)
);

create table ATIVIDADE(
    cod_atividade serial,
    data_hora timestamp,
    tipo varchar(30),
    nome varchar(50),
    descricao varchar(240),
    localizacao varchar(240),/*Geolocalização*/
    cod_usuario int, /*chave estrangeira*/
    primary key(cod_atividade)
);

create table TRABALHO(
    cod_trabalho serial,
    conteudo varchar(240), /*coteudo da postagem (foto, video, texto, etc)*/
    data_hora timestamp,
    tag varchar(30),
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

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

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


