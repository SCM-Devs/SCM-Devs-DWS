# Projet DWS - Scraping et Affichage de Produits

## 📍 Le Principe ?

Ce projet permet de récupérer des données produits à partir du site Extime.com, de les sauvegarder dans un fichier CSV, et de les afficher sur une page web.

Le backend est développé avec Flask, et le frontend permet d'afficher les produits sous forme de cartes avec pagination. Il inclut également un système de recherche par nom de produit.

L'application a pour objectif de manipuler et afficher dynamiquement des données de produits, en offrant des fonctionnalités essentielles telles que la recherche, la modification et la pagination. Nous avons porté une attention particulière à l'expérience utilisateur en optimisant l'affichage et la navigation.

## 👉 Sur l'appli vous pouvez -->

- **Recherche** : Système de recherche permettant de chercher les produits par nom.
- **Vue détaillée des produits** : En cliquant sur un produit, une page détaillée s'affiche avec plus d'informations.
- **Modifier** : Modifier le produit depuis ça fiche produits. Et **Sauvegarder** pour enregistrer les modification.
- **Pagination** : Affichage des produits avec pagination pour éviter de charger toutes les données d'un coup.
- **Scrapper** : Lancer le scraping depuis l'appplication.

## 🔧 Installation

Avant de commencer, vous devez vous assurer que **Python** est installé sur votre machine.

### Installer Python
Si vous n'avez pas Python, vous pouvez le télécharger depuis le site officiel : [https://www.python.org/downloads/](https://www.python.org/downloads/)


### Installer un environnement virtuel
Créez un environnement virtuel pour isoler les dépendances du projet : `python -m venv venv`


### Activer l'environnement virtuel
Sur Windows :
`venv\Scripts\activate`

Sur Mac/Linux :
`source venv/bin/activate`

### Installer les dépendances
 Toujours dans votre terminal, entrer : `pip install -r requirements.txt`

### Lancer l'application
Une fois les dépendances installées, vous pouvez lancer le serveur Flask avec la commande suivante : 

Sur Windows :
`python run.py`

Sur Mac/Linux :
`python3 mon_script.py`

Le serveur sera lancé sur http://127.0.0.1:5000 par défaut ( vous pouvez ouvrir l'application sur le navigateur de votre choix ). Une autre ligne sera visible dans la console pour indiquer l'adresse exacte sur laquelle les appareils connectés au même réseau pourront avoir accès.
Cette ligne commence comme ça : "Application accessible sur : "

### Une fois sur l'application
Avant de lancer l’application, vous devez impérativement exécuter un premier scraping pour créer le fichier CSV contenant les produits.

Nous recommandons de le lancer avant le serveur Flask :
`python extime_scraper/main.py`

## Explication Scraping

Lorsque vous lancez le scraping, le programme recherche sur le site toutes les informations nécessaires et extrait les données des produits dans chaque page des catégories sélectionnées.

Pour chaque produit, il :
- ✅ Télécharge l’image et la convertit en WebP (si elle n’existe pas déjà).
- ✅ Vérifie et élimine les doublons, en ne conservant que l’essentiel.
- ✅ Génère un fichier CSV contenant toutes les informations.

⏳ Durée d’exécution : environ 30 minutes sur Windows, légèrement plus rapide sur Mac.

Malgré nos efforts, notre bot de scraping ne récupère pas toutes les données correctement. Certains produits peuvent être absents, et certaines informations peuvent être incomplètes ou erronées.
Nous avons identifié ces limitations, mais en raison des contraintes de temps, nous n'avons pas pu les corriger entièrement avant la remise du projet.
Ce README vise à être transparent sur l’état actuel du projet et notre volonté de réussir. 

## 📢 Remarque finale
Ceci est le repositiry final que nous utilisons pour livrer le projet. Mais nous avons travailler sur un repository parallèle afin de livrer une version propre. Nous vous mettons tout de même le lien du repository de travaille pour témoigner de nos effort au cours des trois dernière semaine. 
👉 https://github.com/SCM-Devs/SCMDev_Coda_DWS

Ce projet a été réalisé dans un cadre scolaire et noté. Malgré les imperfections, il démontre notre capacité à concevoir un bot de scraping, à exploiter les données récupérées et à les présenter sous forme d’application web.

Merci de votre compréhension et bonne utilisation ! 🚀
