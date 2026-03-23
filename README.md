# 📱 LocalTax

<div align="center">

> Application Android — calcul de taxe locale

<video src="assets/demo.mp4" controls width="1000"></video>

<br/><br/>

![Android](https://img.shields.io/badge/Android-API%2021%2B-3DDC84?style=flat-square\&logo=android\&logoColor=white)
![Java](https://img.shields.io/badge/Java-8%2B-007396?style=flat-square\&logo=openjdk\&logoColor=white)
![Lab](https://img.shields.io/badge/Lab-Mobile%20Android-555?style=flat-square)
![Status](https://img.shields.io/badge/Statut-Complet-success?style=flat-square)

</div>

---

## 🧾 Description

## 🧾 Description

LocalTax est une application Android simple permettant de calculer une taxe locale basée sur :

* la surface du logement (en m²)
* le nombre de pièces
* la présence ou non d’une piscine

L’objectif est de fournir un résultat rapide et clair à l’utilisateur.

---

## ⚙️ Fonctionnalités

* Saisie de la surface
* Saisie du nombre de pièces
* Option "Piscine" (CheckBox)
* Calcul automatique de la taxe
* Affichage du résultat en DH
* Vérification des champs (message Toast si vide)

---

## 🧮 Formule de calcul

```text
Taxe = (surface × 2) + (pièces × 50) + (100 si piscine)
```

---

## 🧑‍💻 Structure du projet

### 🔹 MainActivity.java

Contient :

* La récupération des données utilisateur
* La validation des champs
* Le calcul de la taxe
* L’affichage du résultat

### 🔹 activity_main.xml

Contient l’interface utilisateur :

* 2 champs de saisie (surface, pièces)
* 1 checkbox (piscine)
* 1 bouton (calculer)
* 1 zone d’affichage du résultat

---

## ▶️ Utilisation

1. Lancer l’application
2. Entrer la surface en m²
3. Entrer le nombre de pièces
4. Cocher "Piscine" si applicable
5. Cliquer sur "calculer"
6. Voir le résultat affiché

---

## 🎥 Vidéo de démonstration

Vous pouvez visualiser le test de l'application ici :

```md
[▶️ Voir la vidéo de test](./demo.mp4)
```

📌 Instructions :

* Placez votre fichier vidéo (ex: `demo.mp4`) dans le même dossier que le README
* Adaptez le nom du fichier si nécessaire

💡 Alternative (GitHub avec lien externe) :

```md
[▶️ Voir la vidéo sur Google Drive](https://lien-de-votre-video)
```

---

## 🧪 Cas de test

### ✅ Test 1 : Cas normal

* Surface : 100
* Pièces : 3
* Piscine : Non

Calcul :

```
(100 × 2) + (3 × 50) = 200 + 150 = 350 DH
```

Résultat attendu : **350.00 DH**

---

### ✅ Test 2 : Avec piscine

* Surface : 80
* Pièces : 2
* Piscine : Oui

Calcul :

```
(80 × 2) + (2 × 50) + 100 = 160 + 100 + 100 = 360 DH
```

Résultat attendu : **360.00 DH**

---

### ❌ Test 3 : Champs vides

* Surface : (vide)
* Pièces : 2

Résultat attendu :

* Message Toast : "Remplir tous les champs"

---

### ❌ Test 4 : Valeurs invalides

* Surface : abc
* Pièces : 2

Résultat attendu :

* Crash possible (à améliorer)

💡 Amélioration suggérée : ajouter une gestion d’erreur (try/catch)

---

## 🚀 Améliorations possibles

* Gestion des erreurs (NumberFormatException)
* Ajout d’un design plus moderne (Material UI)
* Sauvegarde des données
* Historique des calculs

---

## 👨‍🎓 Auteur

AMSOU ISMAIL — Lab de développement mobile
