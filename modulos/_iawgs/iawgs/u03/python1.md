---
title: Introducción al despliegue de aplicaciones python
permalink: /iawgs/u03/python1.html
---

## Tarea 1: Entorno de desarrollo 

Vamos a desarrollar la aplicación del [tutorial de django 1.10](https://docs.djangoproject.com/en/1.10/intro/tutorial01/). Vamos a configurar tu equipo como entorno de desarrollo para trabajar con la aplicación, para ello:

* Clona el repositorio de GitHub: [https://github.com/josedom24/django_tutorial](https://github.com/josedom24/django_tutorial).
* Crea un entorno virtual de python3 e instala las dependencias necesarias para que funcione el proyecto (fichero `requierements.txt`).
* Comprueba que vamos a trabajar con una base de datos sqlite (`django_tutorial/\settings.py`). ¿Cómo se llama la base de datos que vamos a crear?
* Crea la base de datos: `python3 manage.py migrate`. A partir del modelo de datos se crean las tablas de la base de datos.
* Crea un usuario administrador: `python3 manage.py createsuperuser`.
* Ejecuta el servidor web de desarrollo y entra en la zona de administración (`\admin`) para comprobar que los datos se han añadido correctamente.
* Crea dos preguntas, con posibles respuestas.
* Comprueba en el navegador que la aplicación está funcionando.

{% capture notice-text %}
En este momento, muestra al profesor la aplicación funcionando. Entrega una documentación resumida donde expliques los pasos fundamentales para realizar esta tarea. (2 puntos)
{% endcapture %}<div class="notice--info">{{ notice-text | markdownify }}</div>

## Tarea 2: Entorno de producción

Vamos a realizar el despliegue de nuestra aplicación en un entorno de producción, para ello vamos a utilizar una instancia del cloud, para ello:

* Instala en el servidor los servicios necesarios (apache2). Instala el módulo de apache2 para ejecutar código python.
* Clona el repositorio en el `DocumentRoot` de tu virtualhost.
* En el entorno de producción no vamos a crear un entorno virtual, vamos a instala django en el sistema: `apt install python-django`.
* Configura un virtualhost en apache2 con la configuración adecuada para que funcione la aplicación. El punto de entrada de nuestro servidor será `django_tutorial/wsgi.py`. Es recomendable que sigas este manual: [https://docs.djangoproject.com/en/1.10/howto/deployment/wsgi/modwsgi/](https://docs.djangoproject.com/en/1.10/howto/deployment/wsgi/modwsgi/). También te puede ayudar este artículo: [Despliegue de aplicación flask en un servidor LAMP](https://plataforma.josedomingo.org/pledin/cursos/flask/curso/u33/) o la primera parte de este otro: [Ejecución de script python](https://plataforma.josedomingo.org/pledin/cursos/apache24/curso/u26/).
* Crea la base de datos.
* Crea un usuario administrador.
* Desactiva en la configuración (fichero `settings.py`) el modo debug a False. Para que los errores de ejecución no den información sensible de la aplicación.
* Muestra la página funcionando.

{% capture notice-text %}
En este momento, muestra al profesor la aplicación funcionando. Entrega una documentación resumida donde expliques los pasos fundamentales para realizar esta tarea. (3 puntos)
{% endcapture %}<div class="notice--info">{{ notice-text | markdownify }}</div>

