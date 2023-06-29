Iniciar o projeto Django
```
Migrando a base de dados do Django 

python manage.py makemigrations
python manage.py migrate
```
Criando e modificando a senha de um super usuario django 

python manage.py createsuperuser
python manage.py changepassword USERNAME

```
django-admin startproject Project .

python manage.py runserver 

django-admin  runserver 

python manager.py startapp home

python manager.py startapp blog 

python manager.py startapp base


```
python -m venv venv
-win -> .\env\Scripts\Activate.ps1 

pip install django
django-admin startproject project .
python manage.py startapp contact
```

pip install django

Configurar o git

```
git config --global user.name 'Feliposen'
git config --global user.email 'felipos.round@gmail.com'
git config --global init.defaultBranch main
# Configure o .gitignore
git init
git add .
git commit -m 'Initial'
git remote add origin git@github.com:Feliposen/Projeto-Agenda-Django-23.git
```


git add .
git commit -m 'Mudei o README.md de comandos'
git log --oneline
git push origin main -u

git graph 
git init
git 
git status 
git add . 
git commit -m "Add INIT 1"
git branch
git status 


'''
python manage.py shell

>>> from contact.models import Contact
>>> Contact
<class 'contact.models.Contact'>
>>> c = Contact(first_name='Gustavo')
>>> c
<Contact: Gustavo >
>>> c.save()
>>> c.last_name = 'Moreira'
>>> c.save()
>>> c.phone ='12345555'
>>> c.save()
>>> c.delete()
(1, {'contact.Contact': 1})
< Contact: Gustavo Moreira> 
>>>
< Contact: Gustavo Moreira> 
>>> c.first_name
'Gustavo'
>>> c.last_name
'Moreira'
>>> c.save()
>>> c = Contact.object.get(id=10)
>>> c.first_name = 'Helena'
>>> c.save()
'''

Trabalhando com o model do Django
```
# Importe o módulo
from contact.models import Contact
# Cria um contato (Lazy)
# Retorna o contato
contact = Contact(**fields)
contact.save()
# Cria um contato (Não lazy)
# Retorna o contato
contact = Contact.objects.create(**fields)
# Seleciona um contato com id 10
# Retorna o contato
contact = Contact.objects.get(pk=10)
# Edita um contato
# Retorna o contato
contact.field_name1 = 'Novo valor 1'
contact.field_name2 = 'Novo valor 2'
contact.save()
# Apaga um contato
# Depende da base de dados, geralmente retorna o número
# de valores manipulados na base de dados
contact.delete()
# Seleciona todos os contatos ordenando por id DESC
# Retorna QuerySet[]
contacts = Contact.objects.all().order_by('-id')
# Seleciona contatos usando filtros
# Retorna QuerySet[]
contacts = Contact.objects.filter(**filters).order_by('-id')

python manage.py collectstatic 