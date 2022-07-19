===========================================
Comandos SQL para criar o banco de dados (Utilisei o phpmyadmin):
===========================================
create table tb_status(
	id int not null primary key auto_increment,
    status varchar(25) not null
);

insert into tb_status(status)values('pendente');
insert into tb_status(status)values('realizado');

create table tb_tarefas(
	id int not null primary key auto_increment,
    id_status int not null default 1,
    foreign key(id_status) references tb_status(id),
	tarefa text not null,
    data_cadastrado datetime not null default current_timestamp
)



===========================================
Dica:
===========================================

Recomendo que salve os arquivos da pasta "app_lista_tarefas" em outro diretório fora do diretório "htdocs" para maior
segurança.
Deixei na mesma pasta para facilitar o uso de quem baixar os códigos pelo github,
mas deixar na mesma pasta assim como está agora pode afetar a segurança do site, 
permitindo que invasores facilmente acessem os dados do administrador.

===========================================