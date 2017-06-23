# RancherOS #  
Configuration for my RancherOS NAS

L'installation sur un disque se fait avec la commande ros install.

Pour rajouter des parmètres et les clés de connexion SSH on peut passer en paramètre le fichier cloud-config.yaml.

**ros install -c cloudconfig.yaml ** 

Genérer une clé SSH 

Sous linux lancer la commande  : **ssh-keygen -t rsa -b 4096 -C "your_email@example.com"** l'adresse mail n'est pas obligatoire mais vous permet d'identifier la clé.


 
