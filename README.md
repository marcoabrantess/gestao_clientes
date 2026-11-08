# Gestao Clientes
Sobre:  
É um sistema simples, feito em Python/Django, de gestao de cadastro de clientes, possui apenas a home e a página de clientes, onde se cadastra um cliente, 
acessa a lista de clientes cadastrados, exclui um cliente cadastrado, busca clientes pelo nome. 
Cada cliente possui apenas um documento, entao, para garantir que nenhum documento seja usado duas vezes, ao criar um cliente, 
deve-se criar um documento e, dessa forma, associar o documento a ele. 
Para fazer login, tem que possuir um superusuario, o usuario e senha sao respectivamente as senhas do mesmo. 
Como é um sistema de teste, os links de redes sociais no rodapé do site, não levam a lugar algum, ja que não é de nenhuma empresa real. 
Data e hora no rodapé do site, é de acordo com a maquina em que o servidor está rodando. 
     
## Para configurar a aplicação no windows:   
1. Abra o terminal e va para o diretorio da aplicação   
2. rode o comando 'python -m venv venv' para criar uma maquina virtual   
3. rode o comando 'venv\Scrpits\activate' para ativá-la   
4. Agora, crie um banco de dados MySQL para a aplicação em si. Caso queira usar um existente, nao precisa seguir esse passo. Em outro  terminal, 
execute os comandos:   
4.1. 'mysql -u root -p'   
4.1.1 - Digite a senha do seu MySQL Server   
4.2 - 'CREATE DATABASE db_mysite;'   
4.3 - 'CREATE USER 'nome_do_usuario'@'localhost' IDENTIFIED BY 'senha';'   
4.4 - 'GRANT ALL ON db_mysite.* TO 'nome_do_usuario'@'localhost';'   
4.5 - 'FLUSH PRIVILEGES;   
5. Execute o comando 'pip install requirements-dev.txt' para instalar o necessário para rodar a aplicação   
6. Copie `.env.example` para `.env` (não commite esse arquivo) e exporte as variáveis no ambiente do processo. `DJANGO_SECRET_KEY` e `DB_PASSWORD` são obrigatórias. `EMAIL_HOST_PASSWORD` só é necessária para envio de email. `DJANGO_DEBUG` é opcional. O arquivo `CRUD/settings.py` lê esses valores do ambiente. Se o nome do banco, o usuário, o host ou a porta forem diferentes, atualize somente esses campos em `settings.py`.   
7. Execute o comando 'python manage.py makemigrations' para realizar as operaões do banco de dados   
8. Execute o comando 'python manage.py migrate' para realizar a criação das tabelas no banco de dados   
9. Execute o comando 'python manage.py createsuperuser' para criar um super usuario   
10. Execute o comando 'python manage.py runserver' para rodar o servidor   

**OBS1:** Certifique-se de que o computador tenha o python, o pip e o MySQL instalado corretamente   
**OBS2:** Para recuperação de senha por email, defina a variável de ambiente `EMAIL_HOST_PASSWORD` e ajuste `EMAIL_HOST_USER` em `settings.py` com o endereço remetente. Não grave a senha no código. Dessa forma, ao utilizar o comando 'Esqueci minha senha' da aplicação, chegará um link no email para poder resetá-la.   

## Para configurar a aplicação no linux\Mac Os:   
1. Abra o terminal e va para o diretorio da aplicação   
2. rode o comando 'python -m venv venv' para criar uma maquina virtual   
3. rode o comando '. venv\bin\activate' para ativá-la   
4. Agora, crie um banco de dados MySQL para a aplicação em si. Caso queira usar um existente, nao precisa seguir esse passo. Em outro  terminal, 
execute os comandos:   
4.1 - 'mysql -u root -p'   
4.1.1 - Digite a senha do seu MySQL Server   
4.2 - 'CREATE DATABASE db_mysite;'     
4.3 - 'CREATE USER 'nome_do_usuario'@'localhost' IDENTIFIED BY 'senha';'     
4.4 - 'GRANT ALL ON db_mysite.* TO 'nome_do_usuario'@'localhost';'   
4.5 - 'FLUSH PRIVILEGES;   
5. Execute o comando 'pip install requirements-dev.txt' para instalar o necessário para rodar a aplicação   
6. Copie `.env.example` para `.env` (não commite esse arquivo) e exporte as variáveis no ambiente do processo. `DJANGO_SECRET_KEY` e `DB_PASSWORD` são obrigatórias. `EMAIL_HOST_PASSWORD` só é necessária para envio de email. `DJANGO_DEBUG` é opcional. O arquivo `CRUD/settings.py` lê esses valores do ambiente. Se o nome do banco, o usuário, o host ou a porta forem diferentes, atualize somente esses campos em `settings.py`.   
7. Execute o comando 'python manage.py makemigrations' para realizar as operaões do banco de dados   
8. Execute o comando 'python manage.py migrate' para realizar a criação das tabelas no banco de dados   
9. Execute o comando 'python manage.py createsuperuser' para criar um super usuario   
10. Execute o comando 'python manage.py runserver' para rodar o servidor   
  
**OBS1:** Certifique-se de que o computador tenha o python, o pip e o MySQL instalado corretamente   
**OBS2:** Para recuperação de senha por email, defina a variável de ambiente `EMAIL_HOST_PASSWORD` e ajuste `EMAIL_HOST_USER` em `settings.py` com o endereço remetente. Não grave a senha no código. Dessa forma, ao utilizar o comando 'Esqueci minha senha' da aplicação, chegará um link no email para poder resetá-la.   
