# mini-projet-docker
Ce projet a pour objectif de dockeriser une application web composée de deux modules : une API développée avec Flask et une interface utilisateur en PHP. L’ensemble est conçu pour une entreprise fictive nommée POZOS.

🛠️ Stack technique
Docker

Docker Compose

Flask (API REST)

PHP / Apache (interface front-end)

CentOS (VM recommandée pour l’exécution)

📁 Structure du projet
Dockerfile : construction de l’image Docker pour l’API Flask

docker-compose.yml : orchestration du déploiement des services Flask et PHP

requirements.txt : dépendances Python

student_age.json : fichier de données JSON (étudiants)

student_age.py : script Python de l’API

index.php : page d’accueil du site PHP

/website/ : dossier monté contenant les fichiers PHP

⚙️ Fonctionnalités
L’API Flask retourne une liste d’étudiants au format JSON

Le front-end PHP interroge cette API et affiche les données

Mise en place de volumes, ports exposés et variables d’environnement

Déploiement automatisé avec Docker Compose

🚀 Lancement du projet
Construire l’image de l’API :

bash
Copier
Modifier
docker build -t student-api .
Démarrer l’ensemble des services :

bash
Copier
Modifier
docker-compose up -d
Tester l’API via curl :

bash
Copier
Modifier
curl -u toto:python http://localhost:5000/pozos/api/v1.0/get_student_ages
Accéder à l’interface web via le navigateur sur le port défini dans docker-compose.yml

🎓 Objectifs pédagogiques
Appliquer les bonnes pratiques en matière de conteneurisation avec Docker

Structurer une application multi-conteneurs avec Docker Compose

Maîtriser la gestion des volumes, réseaux, ports et services

Comprendre l’architecture logicielle découplée
