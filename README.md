# capstone_project_Part3
C'est quoi Kompose ? C'est un outil de conversion de tout ce qui compose (notamment Docker Compose) en orchestrateurs de conteneurs (Kubernetes ou OpenShift). Vous trouverez plus d'informations sur le site web de Kompose à http://kompose.io.

Kubernetes définit un jeu d'outils ("primitives") qui, ensemble, fournissent des mécanismes pour déployer, maintenir et mettre à l’échelle des applications. Ces éléments qui composent Kubernetes sont conçus pour être combinés et extensibles et donc permettre de supporter une grande variété de charge de travail. Cette extensibilité est fournie en grande partie par l'API de Kubernetes, qui est utilisée par les composants internes aussi bien que par les extensions et les conteneurs tournant sur Kubernetes15.

####################Partie 3 : Convertir un fichier Docker Compose en ressources Kubernetes####################

Dans cette partie, on va traduire les services Compose en objets Kubernetes à l'aide de kompose. On a utiliser les définitions d'objet fournies par kompose comme point de départ et effectuerez des ajustements pour s'assurer que notre configuration utilisera Secrets, Services et PersistentVolumeClaims de la manière attendue par Kubernetes. À la fin, on disposra disposerez d'une application Node.js à instance unique avec une base de données MongoDB exécutée sur un cluster Kubernetes. Cette configuration reflétera la fonctionnalité du code décrit dans Conteneuriser une application Node.js avec Docker Compose et constituera un bon point de départ pour créer une solution prête pour la production qui s'adaptera à vos besoins.

Pour la réalisation j'ai suivi les étapes citer ci-dessous: 

  * Cloner et empaqueter l'application
  * Traduire les services Compose en objets Kubernetes avec kompose
  * Création de secrets Kubernetes
  * Création du service de base de données et d'un conteneur d'initialisation d'application
  * Modification de PersistentVolumeClaim et exposition de l'interface de l'application
  * Démarrage et accès à l'application
  
![image](https://user-images.githubusercontent.com/80095967/150679645-4bae5835-17c6-4b80-9c6e-597e72769552.png)
![image](https://user-images.githubusercontent.com/80095967/150679670-e562f186-973b-4fdf-8354-b279f1ba0341.png)
![image](https://user-images.githubusercontent.com/80095967/150679682-130dfad0-8ae8-423a-b97d-885606df3db0.png)

