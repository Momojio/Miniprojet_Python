# Miniprojet_Python
Ce projet implémente un système avancé de détection et suivi de multiples visages en temps réel utilisant une combinaison sophistiquée de techniques de vision par ordinateur. Le système intègre le classificateur en cascade de Haar d'OpenCV pour la détection initiale et les trackers par corrélation de dlib pour un suivi robuste et performant.

Fonctionnalités

•	Suivi Multi-Visages en Temps Réel : Détecte et suit plusieurs visages dans des flux vidéo en temps réel
•	Approche Hybride : Combine les classificateurs Haar d'OpenCV pour la détection avec le suivi par corrélation de dlib pour des performances robustes
•	Gestion Intelligente des Traqueurs : Crée et supprime automatiquement les traqueurs lorsque les visages entrent et quittent le champ de vision
•	Détection Adaptative : Effectue une détection complète périodiquement pour corriger la dérive du suivi
•	Contrôle de Qualité : Surveille la qualité du suivi et supprime les traqueurs non fiables

Technologies Utilisées

•	Python 3.6+ : Langage de programmation principal
•	OpenCV : Bibliothèque de vision par ordinateur pour le traitement d'images et la détection de visages
•	dlib : Boîte à outils d'apprentissage automatique pour un suivi haute performance

Fonctionnement

•	Détection de Visages : Utilise des classificateurs en cascade Haar pour détecter les visages
•	Initialisation des Traqueurs : Crée un traqueur par corrélation dlib pour chaque visage détecté
•	Suivi Continu : Les traqueurs suivent les visages entre les cycles de détection
•	Correction Périodique : Effectue une détection complète toutes les 15 images pour corriger les erreurs de suivi
•	Gestion Dynamique : Ajoute des traqueurs pour les nouveaux visages et supprime ceux des visages perdus
