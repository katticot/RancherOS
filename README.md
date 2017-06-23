# RancherOS #  
Configuration for my RancherOS NAS

L'installation sur un disque se fait avec la commande ros install.

Pour rajouter des parmètres et les clés de connexion SSH on peut passer en paramètre le fichier cloud-config.yaml.

**ros install -c cloudconfig.yaml ** 

## Genérer une clé SSH 

Sous linux lancer la commande  :  l'adresse mail n'est pas obligatoire mais vous permet d'identifier la clé.

```sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Generating public/private rsa key pair.
 ```

Une fois la clé généré il faut choisir l'endroit ou elle est sauvegardée
```sh
Enter file in which to save the key (/home/user/.ssh/id_rsa):
 ```
 
 Si vous le souhaitez vos pouvez sécuriser votre clé privé avec une *passphrase* , elle ne sera pas utilisable sans, c'est facultatif **mais fortement conseillé.
 
 ```sh
Enter passphrase (empty for no passphrase):
 ```
  Votre clé est générée !!
 ```sh
 Your identification has been saved in /home/user/key_RSA.
Your public key has been saved in /home/user/key_RSA.pub.
The key fingerprint is:
58:a3:05:0a:02:2e:3a:79:1c:0c:08:20:f5:9b:74:3a your_email@example.com
The key's randomart image is:
+---[RSA 4096]----+
|%.o   .          |
|++ o . .         |
|..o + . +        |
|oo o = = .       |
|+ o E o S        |
| o   .           |
|                 |
|                 |
|                 |
+-----------------+
```

Vous disposez maintenant de deux fichiers, la clé publique "key_RSA" et la clé publique "key_RSA.pub".

Votre clé privé vous sera necessaire pour vous connecter en SSH gardez la précieusement, encore plus si vous n'avez pas de passphrase car n'importe qui pourra se connecter à votre machine si il possède cette clé.

La clé publique est l'empreinte de la clé privé, c'est elle que l'on va utiliser dans le [config-cloud.xml](../master/cloud-config.yaml) 
