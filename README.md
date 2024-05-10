# Projet Ansible pour Déploiement d'Application PHP
Ce projet utilise Ansible pour automatiser le déploiement et la gestion de la configuration d'une application PHP sur des serveurs de production et de staging.

# Auteur
 - Salim Abi = (https://github.com/salimabi68/projet-ansible-lazy)

## Prérequis
- Ansible 2.9 ou version ultérieure.
- Serveurs avec Debian.
- Accès SSH configuré pour les machines cibles.
- Git, PHP et MySQL doivent être installés sur les serveurs cibles pour le déploiement.

## Configuration
- Ansible: Configurer les fichiers inventory pour pointer vers vos serveurs de staging et de production.
- Variables: Définir les variables nécessaires dans les dossiers group_vars ou host_vars selon l'environnement

## Déploiement + nginx
-  Pour le staging :
```
  ansible-playbook -i ansible/inventories/hosts.yml ansible/webservers.yml
```

- Pour la production :
``` 
 ansible-playbook -i ansible/inventories/hosts.yml ansible/webservers.yml
```

## Lancement de l'application
```
# Naviguer dans le répertoire de l'application
cd /var/www/app

# Lancer le serveur de développement PHP
php -S localhost:8000
```
