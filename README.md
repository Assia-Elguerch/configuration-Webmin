# Configuration de Webmin sur Linux Debian 🖥️

## Introduction à Webmin
Webmin est un outil de configuration système basé sur le web conçu pour simplifier la gestion des serveurs Unix et Linux. Il fournit une interface conviviale permettant aux administrateurs système de configurer et de gérer divers aspects du système, tels que les utilisateurs, les services, les pare-feu, les fichiers de configuration et bien plus encore, à travers un navigateur web.

![image](https://duckduckgo.com/i/056fc676.png)

https://webmin.com/

## Téléchargement et Installation de Webmin
- Avant de commencer à installer Webmin, assurez-vous de mettre à jour le système et d'installer les prérequis nécessaires :

```bash
sudo apt update && sudo apt upgrade
```

- Téléchargez la dernière version de Webmin depuis son site officiel et installez-la en utilisant les commandes suivantes :

```bash
curl -o setup-repos.sh https://raw.githubusercontent.com/webmin/webmin/master/setup-repos.sh
sh setup-repos.sh
apt-get install webmin --install-recommends

```
> [!IMPORTANT]
> Le fichier de configuration principal de Webmin est miniserv.conf.

## Accès à Webmin
- Après l'installation, assurez-vous de permettre l'accès à Webmin via le pare-feu en ouvrant le port 10000 :

```bash
sudo ufw allow 10000/tcp
```
- Démarrez le service Webmin et accédez à l'interface Webmin en saisissant l'URL suivante dans votre navigateur :

```bash
sudo systemctl start webmin.service
```

https:// Your-Server-IP :10000

![image](https://webmin.com/images/screenshots/dark/1-dashboard.png)




