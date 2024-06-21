# Comandos básicos MySql para utilizar no terminal

## 1 - Conexão ao Banco de Dados

### Conectar ao MySQL/MariaDB
- mysql -u [usuário] -p
- mysql -u [usuário] -p[senha]
- mysql -u [usuário] -p -h [hostname]


## 2 - Comandos Básicos:

### Mostrar bancos de dados
- SHOW DATABASES;

### Selecionar banco de dados
- USE [nome_do_banco];

### Mostrar tabelas no banco de dados selecionado
- SHOW TABLES;

### Descrever a estrutura de uma tabela
- DESCRIBE [nome_da_tabela];
- SHOW COLUMNS FROM [nome_da_tabela];

### Mostrar usuários
 - SELECT user, host FROM mysql.user;

### Mostrar status do servidor
- STATUS;

## 3 - Gerenciamento de Banco de Dados

### Criar um banco de dados
- CREATE DATABASE [nome_do_banco];

### Apagar um banco de dados
- DROP DATABASE [nome_do_banco];

### Renomear um banco de dados (apenas MariaDB)
- RENAME DATABASE [nome_antigo] TO [nome_novo];

## 4 - Gerenciamento de Tabelas

### Criar uma tabela
- CREATE TABLE [nome_da_tabela] (
    [nome_da_coluna] [tipo_de_dado] [opções],
    ...
);

### Apagar uma tabela
DROP TABLE [nome_da_tabela];

# Renomear uma tabela
RENAME TABLE [nome_antigo] TO [nome_novo];

# Adicionar coluna
ALTER TABLE [nome_da_tabela] ADD [nome_da_coluna] [tipo_de_dado] [opções];

# Apagar coluna
ALTER TABLE [nome_da_tabela] DROP COLUMN [nome_da_coluna];

# Modificar coluna
ALTER TABLE [nome_da_tabela] MODIFY [nome_da_coluna] [novo_tipo_de_dado] [novas_opções];
Consultas de Dados

# Selecionar dados
SELECT [colunas] FROM [tabela] WHERE [condições];

# Inserir dados
INSERT INTO [tabela] ([colunas]) VALUES ([valores]);

# Atualizar dados
UPDATE [tabela] SET [coluna] = [valor] WHERE [condições];

# Apagar dados
DELETE FROM [tabela] WHERE [condições];

6 - Índices

# Criar índice
CREATE INDEX [nome_do_indice] ON [nome_da_tabela] ([colunas]);

# Apagar índice
DROP INDEX [nome_do_indice] ON [nome_da_tabela];

7 - Transações:

# Iniciar transação
START TRANSACTION;

# Confirmar transação
COMMIT;

# Reverter transação
ROLLBACK;
Usuários e Permissões

8 - Copiar código
# Criar usuário
CREATE USER '[usuário]'@'[host]' IDENTIFIED BY '[senha]';

# Apagar usuário
DROP USER '[usuário]'@'[host]';

# Conceder permissões
GRANT [tipo_de_permissão] ON [banco_de_dados].[tabela] TO '[usuário]'@'[host]';

# Revogar permissões
REVOKE [tipo_de_permissão] ON [banco_de_dados].[tabela] FROM '[usuário]'@'[host]';

# Mostrar permissões
SHOW GRANTS FOR '[usuário]'@'[host]';
Backup e Restauração
bash
Copiar código
# Backup de um banco de dados
mysqldump -u [usuário] -p [nome_do_banco] > [arquivo.sql]

# Restauração de um banco de dados
mysql -u [usuário] -p [nome_do_banco] < [arquivo.sql]
Utilitários
sql
Copiar código
# Mostrar processo atual
SHOW PROCESSLIST;

# Mostrar variáveis de sistema
SHOW VARIABLES;

# Mostrar status do servidor
SHOW STATUS;

# Encerrar uma sessão de conexão
EXIT;
Esta lista cobre os comandos mais utilizados no MySQL/MariaDB. Se precisar de comandos mais avançados ou específicos, sinta-se à vontade para perguntar!









