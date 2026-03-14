# **🛠️ Portail Ressources Fablab**

Une application web interactive et responsive permettant aux membres d'un Fablab de consulter, filtrer et trouver facilement des ressources documentaires (tutoriels vidéo, manuels PDF, sites web, playlists).

## **✨ Fonctionnalités**

* **Recherche en temps réel** : Trouvez instantanément un document par son titre ou sa description.  
* **Filtres avancés** :  
  * Par format (Vidéo, Playlist, PDF, Web)  
  * Par catégorie (Impression 3D, Électronique, Fraiseuse CNC, etc.)  
  * Par niveau (Débutant, Intermédiaire, Expert)  
* **Design Responsive** : Interface optimisée pour les ordinateurs, tablettes et smartphones (avec gestion des événements tactiles).  
* **Gestion simplifiée (No-Code)** : Les données sont alimentées par un simple fichier Google Sheets (exporté en CSV), permettant aux gérants du Fablab d'ajouter des ressources sans toucher au code.

## **🔗 Lien de l'application**

L'application est déployée et accessible ici : **\[Insérez votre lien GitHub Pages ici, ex: https://atelier3dprog.github.io/Portail_Doc_Atelier3dprog//\]**

## **🗂️ Comment mettre à jour les ressources ?**

Les données de ce portail proviennent d'un fichier **Google Sheets**. Pour ajouter, modifier ou supprimer un document, il suffit de modifier le tableau Google Sheets. Les changements apparaîtront automatiquement sur le site.

### **Structure requise du tableau :**

Votre Google Sheets doit obligatoirement contenir ces colonnes sur la première ligne (en minuscules) :

| id | type | category | niveau | title | url | description |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | video | Impression 3D | Débutant | Nom de la vidéo | https://... | Description courte... |
| 2 | pdf | Sécurité | Expert | Manuel Trotec | https://... | Consignes de sécu... |

*Notes sur les colonnes :*

* **type** : Doit être obligatoirement video, playlist, pdf ou web pour afficher la bonne icône.  
* **niveau** : Recommandé d'utiliser Débutant, Intermédiaire ou Expert (génère des badges de couleur).  
* **url** : Pour les PDF hébergés sur Google Drive, assurez-vous que le lien est réglé sur "Tous les utilisateurs disposant du lien".

## **💻 Installation en local (Pour les développeurs)**

Si vous souhaitez modifier le code, l'interface ou ajouter de nouvelles fonctionnalités, voici comment faire tourner le projet sur votre machine.

### **Prérequis**

* [Node.js](https://nodejs.org/) (inclut npm)  
* [Git](https://git-scm.com/)

### **Commandes d'installation**

1. **Cloner le dépôt :**  
   git clone \[https://github.com/VOTRE\_PSEUDO/portail-fablab.git\](https://github.com/VOTRE\_PSEUDO/portail-fablab.git)  
   cd portail-fablab

2. **Installer les dépendances :**  
   npm install

3. **Lancer le serveur de développement :**  
   npm run dev

   *L'application sera accessible sur http://localhost:5173/.*

## **🚀 Déploiement**

Ce projet est configuré pour être déployé gratuitement sur **GitHub Pages**.

Pour mettre à jour la version en ligne après avoir modifié le code source :

1. Assurez-vous d'avoir sauvegardé (commit) vos modifications sur Git :  
   git add .  
   git commit \-m "Mise à jour de l'interface"  
   git push origin main

2. Lancez le script de déploiement automatique :  
   npm run deploy

   *Patientez 1 à 2 minutes, et la version en ligne sera mise à jour \!*

## **🛠️ Technologies utilisées**

* **React** (via Vite)  
* **Tailwind CSS v4** pour le style  
* **Lucide React** pour les icônes vectorielles  
* **gh-pages** pour le déploiement