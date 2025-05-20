# 📦 Mini-projet Docker – Student List App

Ce projet a pour but de **dockeriser une application web** composée de deux parties :
- Une **API** développée avec **Flask** (Python)
- Un **front-end** en **PHP** avec Apache

Le tout est orchestré avec **Docker Compose**, pour simuler une architecture déployée proprement.  
Projet réalisé pour une entreprise fictive : **POZOS**.

---

## 🛠️ Stack technique

- 🐳 Docker
- 🧩 Docker Compose
- 🐍 Flask (API REST)
- 🐘 PHP / Apache (interface utilisateur)
- 💽 CentOS (VM recommandée)

---

## 📁 Structure des fichiers

| Fichier / Dossier        | Rôle                                                                 |
|--------------------------|----------------------------------------------------------------------|
| `Dockerfile`             | Création de l’image Docker pour l’API Flask                         |
| `docker-compose.yml`     | Déploiement orchestré de l’API + interface PHP                      |
| `requirements.txt`       | Dépendances Python pour Flask                                        |
| `student_age.json`       | Données des étudiants (fichier JSON)                                |
| `student_age.py`         | Script Flask fournissant l’API                                      |
| `index.php`              | Interface utilisateur qui consomme l’API                            |
| `/website/`              | Dossier contenant les fichiers du front PHP                         |

---

## ⚙️ Fonctionnalités

- L’**API Flask** fournit des données sur les étudiants au format JSON
- L’**interface PHP** appelle cette API et affiche les résultats
- Utilisation de :
  - **Volumes Docker**
  - **Ports exposés**
  - **Variables d’environnement**
- Déploiement complet orchestré via **Docker Compose**

---

## 🚀 Lancement du projet

### 1. Construire l’image Docker pour l’API
```bash
docker build -t student-api .
