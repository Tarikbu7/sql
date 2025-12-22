# Chapitre 3 – Manipuler un fichier de modélisation

## 🎯 Objectif pédagogique
Être capable d’utiliser un **outil de modélisation** pour créer, modifier et exporter un fichier contenant un **MCD** et un **MLD**, afin de préparer la création d’une base de données SQL.

---

## 📚 Concepts abordés
- Utilisation d’un logiciel de modélisation (**Looping**, **Draw.io**, etc.)
- Création d’entités et d’attributs dans un outil graphique
- Ajout des relations et des cardinalités
- Exportation en image ou en script SQL
- Vérification de la cohérence des modèles

---

## 🧠 Explication théorique
Un **fichier de modélisation** permet de conserver une trace claire, structurée et modifiable de la base de données avant son implémentation.

Des outils comme **Looping**, **MySQL Workbench** ou **Draw.io** facilitent la création visuelle des **MCD** et **MLD**.  
Ces fichiers servent de **référence documentaire** avant le développement de la base.

### ✅ Avantages
- Organisation claire des entités et des relations
- Prévisualisation des contraintes
- Exportation en image ou en format SQL pour gagner du temps

---

## 🛠 Tutoriel pratique

### Résumé du travail
Créer un **MCD de blog** dans un outil de modélisation et l’exporter.

### Étape 1 : Installer un outil de modélisation
- Télécharger **Looping** (Windows)
- Ou utiliser **Draw.io** en ligne

### Étape 2 : Créer les entités
- Ajouter les entités :
  - Utilisateur
  - Article
  - Commentaire
- Pour chaque entité, ajouter les attributs (id, nom, email, etc.)

### Étape 3 : Définir les relations
Créer les relations suivantes :
- Utilisateur — *rédige* — Article **(1,N)**
- Article — *reçoit* — Commentaire **(1,N)**

### Étape 4 : Exporter le MCD
- Sauvegarder le fichier :
  - `.loop` (Looping)
  - `.drawio` (Draw.io)
- Exporter une image (**PNG**) pour la documentation

### Étape 5 : (Optionnel) Générer le MLD
- Certains outils permettent d’exporter directement un **script SQL** à partir du modèle

---

## 🧾 Résumé et points-clés
- Le fichier de modélisation est un **document pivot** avant le SQL
- Les outils de modélisation facilitent la création, la lecture et l’édition des **MCD / MLD**
- L’exportation en image ou en SQL permet un **gain de temps** pour la suite du projet
