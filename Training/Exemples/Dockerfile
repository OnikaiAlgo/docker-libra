# On se base sur une image à taille réduite, ici
# Alpine Linux en version 3.20
FROM alpine:3.20
# On installe les dépendances de notre application
RUN apk add python3
# On créait l’utilisateur “myuser” avec des droits standards
RUN adduser -D -s /bin/sh myuser
# On bascule sur l’utilisateur “myuser”
USER myuser
# On copie les sources de notre application dans le répertoire “app”
# du $HOME de notre nouvel utilisateur
COPY ./app /home/myuser/app
# On définit le répertoire /home/myuser/app comme répertoire
# de travail
WORKDIR /home/myuser/app
# On définit la commande exécutée au lancement
# du conteneur, ici une application Python.
CMD ["python3", "app.py"]