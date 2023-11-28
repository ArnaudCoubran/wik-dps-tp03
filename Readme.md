ReadMe.md

# Ce fichier YAML est une configuration pour Docker Compose, utilisé pour orchestrer des conteneurs Docker. Voici une explication des différentes sections de ce fichier :

Version de l'API Docker Compose:

Utilise la version 3.8 de l'API Docker Compose.
Services:

Déclare un service nommé my_app.
Build:

Spécifie le contexte de build comme étant le répertoire actuel (.).
Utilise le fichier Docker (single-stage.dockerfile) pour construire l'image Docker.
Exposition de ports:

Expose le port 8080 sur le réseau du conteneur.
Redémarrage automatique:

Configure le service pour redémarrer toujours (restart: always) en cas d'arrêt inattendu.
Variables d'environnement:

Définit une variable d'environnement PORT avec la valeur 8080.
Réseau:

Attache le service au réseau nommé front-network.
Image Docker:

Utilise l'image Docker nginx:latest.
Montage de volumes:

Montre le fichier ./nginx.conf depuis le répertoire actuel de l'hôte vers /etc/nginx/nginx.conf dans le conteneur en mode lecture seule (ro).
Port-forwarding:

Configure le port-forwarding entre le port 8081 de l'hôte et le port 80 du conteneur.
Dépendances:

Déclare que le service my_app doit être prêt avant que le service my_app ne démarre.
Réseaux:

Attache le service au réseau nommé front-network.
Déclaration des réseaux:

Déclare un réseau nommé front-network avec le driver bridge.