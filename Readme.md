![Logo Perriercreatif](http://perriercreatif.free.fr/images/logoperriercreatiffinal.png)  
by perriercreatif

[![build](https://travis-ci.org/ikatyang/emoji-cheat-sheet.svg?branch=master)](https://travis-ci.org/ikatyang/emoji-cheat-sheet)

Simplon Online Module
========


PHP blog with Symfony 4 with security administration!


Summary
--------
* Operating instructions


Operating instructions
--------------------
* open the console at the root of the project and type ```composer update``` 

![image01](SymfonyMasterClassAdmin/public/imagesReadme/01-composer-update.png)

* open the .env file to modify these lines with your phpMysql login.
```DATABASE_URL=mysql://Identifiant:MotDePasse@127.0.0.1:3306/masterclasssymfony``` 

![image02](SymfonyMasterClassAdmin/public/imagesReadme/02-files-env.png)

* execute the following command ```php bin/console doctrine:database:create``` which will create a database with the value of your database name.

![image03](SymfonyMasterClassAdmin/public/imagesReadme/03-create-database.png)

* execute the following command ```php bin/console make:migration``` it will create a migration file.

![image04](SymfonyMasterClassAdmin/public/imagesReadme/04-create-files-migration.png)

* execute the following command ```php bin/console doctrine:migrations:migrate``` ( this command fills your BDD with the data in the migration file that the command ```php bin/console make:migration``` to create sooner)

![image05](SymfonyMasterClassAdmin/public/imagesReadme/05-import-files-migration-BDD.png)

* execute the following command ```php bin/console server:run``` and click on http://127.0.0.1:8000

![image02](SymfonyMasterClassAdmin/public/imagesReadme/06-start-server.png)

* la page d'accueil du blog s'affiche sur votre navigateur par default

![image02](SymfonyMasterClassAdmin/public/imagesReadme/07-home-page.png)

* click on " Créer un article " you will arrive on the admin login page

![image02](SymfonyMasterClassAdmin/public/imagesReadme/08-login.png)

* the login and password is in the config/packages/security.yaml file 

![image02](SymfonyMasterClassAdmin/public/imagesReadme/09-login-password.png)

you can change these lines:

```
providers:
        in_memory:
            #{ memory: ~ }
            memory:
                users:
                    ryan:
                        password: ryanpass
                        roles: 'ROLE_ADMIN'
```

* http://127.0.0.1:8000/bo/update/{id} to modify a post ( {id} replace by the id number of the post to be modified example: http://127.0.0.1:8000/bo/update/1)

* http://127.0.0.1:8000/blog/{id} to view a post ( {id} replace by the id number of the post to view example: http://127.0.0.1:8000/blog/1)

* http://127.0.0.1:8000/bo/delete/{id} to delete a post ( {id} replace with the id number of the post to delete example: http://127.0.0.1:8000/bo/delete/1)


Now here you could explore the blog created, modify or delete as you wish.



