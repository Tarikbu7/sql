# Chapitre 1 – Identifier les entités et relations

## 🎯 Objectif pédagogique

L’objectif de ce chapitre est d’apprendre à **analyser un besoin fonctionnel** afin d’identifier correctement :

* les **entités**,
* leurs **attributs**,
* et les **relations** entre elles,

dans le cadre de la conception d’une **base de données relationnelle**.

---

## 📚 Concepts abordés

### 🔹 Qu’est-ce qu’une entité ?

Une **entité** représente un objet ou une notion importante du système à gérer.

**Exemples :**

* Utilisateur
* Article
* Commentaire
* Commande

Chaque entité correspond généralement à une **table** dans une base de données.

---

### 🔹 Notion d’attributs

Les **attributs** sont les propriétés qui décrivent une entité.

**Exemple :**

* Entité **Utilisateur** : id, nom, email, mot_de_passe
* Entité **Article** : id, titre, contenu, date_pub

Chaque entité possède au minimum un **identifiant unique (clé primaire)**.

---

### 🔹 Relations entre entités

Une **relation** décrit le lien logique entre deux entités.

Types de relations courantes :

* **1–1** : une occurrence correspond à une seule autre
* **1–N** : une occurrence correspond à plusieurs autres
* **N–N** : plusieurs occurrences correspondent à plusieurs autres

---

### 🔹 Cardinalités et contraintes

Les **cardinalités** indiquent combien de fois une entité peut être liée à une autre :

* **0** : facultatif
* **1** : obligatoire
* **N** : plusieurs

Elles permettent de définir les règles métier du système.

---

## 🧠 Explication théorique

Une entité représente un objet métier principal à gérer dans le système.
Chaque entité est décrite par des attributs.

Les relations permettent de lier ces entités entre elles.

**Exemples :**

* Un utilisateur peut rédiger **plusieurs articles** → relation **1-N**
* Un article peut recevoir **plusieurs commentaires** → relation **1-N**

Les cardinalités précisent le nombre minimum et maximum de liens possibles entre entités.

---

## 🛠 Tutoriel pratique – Exemple d’un blog

### 📖 Scénario

> « Un site de blog contient des utilisateurs qui rédigent des articles. Les lecteurs peuvent laisser des commentaires sur ces articles. »

---

### ✏️ Étape 1 : Identifier les entités

À partir du scénario, on identifie les objets principaux :

* **Utilisateur**
* **Article**
* **Commentaire**

---

### ✏️ Étape 2 : Identifier les attributs

**Utilisateur**

* id
* nom
* email
* rôle

**Article**

* id
* titre
* contenu
* date_pub

**Commentaire**

* id
* contenu
* auteur
* date

---

### ✏️ Étape 3 : Identifier les relations

* **Utilisateur → Article** :

  * Un utilisateur peut rédiger plusieurs articles
  * Relation **1-N**

* **Article → Commentaire** :

  * Un article peut recevoir plusieurs commentaires
  * Relation **1-N**

---

### 📊 Étape 4 : Table d’analyse

| Entité      | Attributs clés               | Relations                     |
| ----------- | ---------------------------- | ----------------------------- |
| Utilisateur | id, nom, email, mot_de_passe | Rédige des articles (1-N)     |
| Article     | id, titre, contenu, date_pub | Reçoit des commentaires (1-N) |
| Commentaire | id, contenu, auteur, date    | Appartient à un article (N-1) |

---

## 🧾 Résumé – Points clés

* Une **entité** = un objet métier principal
* Un **attribut** = une propriété de l’entité
* Une **relation** = un lien entre entités
* La **cardinalité** définit le nombre de liens possibles
* Cette étape est essentielle pour construire un **MCD (Modèle Conceptuel de Données)**

➡️ Une bonne identification des entités et relations garantit une base de données claire, cohérente et évolutive.
