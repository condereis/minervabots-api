# API MinervaBots #

## Funcionalidades ##

* Autenticação
* Gerenciamento de Membros
* Gerenciamento de Projetos
* Gerenciamento de Inventário


## Local Set up (Unix) ##

### Virtual Enviroment ###
O uso de um ambiente virtual é aconselhado para manter as dependências usadas por diferentes pacotes em lugares diferentes. A tool virtualenv cria diferentes ambientes virtuais em python. 

* Instalar virtualenv e virtualenvwrapper;
```
#!bash
$ pip install virtualenv
```

* Criar pasta para o projeto e um ambiente virtual dentro da mesma;

```
#!bash
$ mkdir env
$ cd env
$ virtualenv env
```
* Entrar no ambiente virtual;
```
#!bash
$ source env/bin/activate
```

### Configuração do projeto ###
* Clonar o repositório para a pasta do projeto;
```
#!bash
$ git clone https://github.com/condereis/minervabots-api.git
```

* Instalar dependências;
```
#!bash
$ cd pinpeopleapi
$ pip install -r requirements.txt
```

* Configurar settings (Ambiente Local);
```
#!bash
$ cp MinervaBotsAPI/settings/local.py-template MinervaBotsAPI/settings/env.py
```

* Criar tabelas do DB e super usuário;
```
#!bash
$ python manage.py migrate
$ python manage.py createsuperuser
```

* Rodar projeto
```
#!bash
$ python manage.py runserver
```

O projeto já estará rodando em http://127.0.0.1:8000/


## Contato ##

* Rafael L. C. Reis - rafael.lcreis@gmail.com