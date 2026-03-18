# cahier-des-charge
1. Présentation générale du projet
1.1 Nom du projet

Tap’Trash
1.2. Nom/Prénom de chaque membre d'équipe
Heloise Abel 
Lorenzo
Aksil
Antonin

1.3 Description générale du jeu
 le joueur contrôle un déchet volant (bouteille/canette) et doit le guider jusqu’à la poubelle de recyclage.
•	Objectif : atteindre la poubelle (ou faire le meilleur score).
•	Pour gagner : appuyer pour faire monter le déchet, passer entre les obstacles, ne pas toucher le sol ni les murs, puis arriver dans la poubelle.
•	Déroulement : le déchet avance tout seul, des obstacles arrivent, chaque passage réussi donne des points ; collision = perdu ; poubelle atteinte = gagné.

2. Public visé
Le jeu s’adresse à des enfants de 6 à 10 ans.
•	Règles simples : un seul objectif (“aller à la poubelle”), une action principale (appuyer = monter).
•	Interface lisible : gros boutons/texte, peu d’éléments à l’écran, pictogrammes.
•	Vocabulaire compréhensible : mots courts (“Bravo !”, “Rejouer”, “Poubelle”, “Point”).
•	Feedback visuel clair : couleurs vives pour les zones, animations de réussite, message en cas d’erreur, son/étoiles quand on marque un point.


3. Trajectoire choisie
La trajectoire est le cœur technique de votre jeu.
3.1 Choix de la trajectoire
Trajectoire gravitationnelle : le déchet tombe avec la gravité et remonte quand le joueur appuie.
3.2 Paramètres et modélisation
Paramètres : y (position), vy (vitesse verticale), g (gravité), jump (impulsion), dt (temps).  Modèle : chaque frame vy += g, puis y += vy. Appui joueur : vy = -jump.
À l’écran : défilement horizontal constant + mouvement vertical en courbe selon les appuis.

3.3 Sources et ressources utiles (trajectoires)
Sites web pédagogiques :
•	Simulateur de lancer de projectile (trajectoire parabolique) : https://www.vmaths.fr/apps/simulateur-lancer-projectile
•	Programmation et mouvement (physique + calcul numérique) : https://info.blaisepascal.fr/nsi-mouvement/
•	Simulation du mouvement d’un projectile en Python (Unisciel) : https://ressources.unisciel.fr/algoprog/s81simul/emodules/si02mexerc1/res/si02exerc1-enonce-py-xxx.pdf

4. Interface graphique
Votre jeu doit comporter une interface graphique.
4.1 Bibliothèques Python possibles

•	Pygame : idéale pour les jeux 2D et animations
4.2 Ressources utiles (bibliothèques Python)
•	Pygame : https://www.pygame.org/docs/
4.3 Justification du choix
•	Pour ce projet, nous utiliserons la bibliothèque Pygame, car elle est spécialement conçue pour le développement de jeux en 2D et permet de gérer facilement les interactions, les animations et les événements clavier/souris..
4.4 Description de l’interface
 Écran principal :
Une zone de jeu 2D où le personnage se déplace, des déchets tombent du ciel et des poubelles sont placées en bas de l’écran.
Boutons :
Aucun bouton. Le joueur utilise le clavier pour se déplacer et la souris pour ramasser les déchets.
 Affichage du score :
Le score est affiché en haut de l’écran et augmente lorsque le déchet est déposé dans la bonne poubelle.
Messages au joueur :
Le score et les noms des poubelles sont affichés pour guider le joueur.  
 <img width="900" height="527" alt="image" src="https://github.com/user-attachments/assets/4c76984d-8e8f-466f-b1cf-48551a1b6288" />

5. Fonctionnalités du jeu
5.1 Fonctionnalités principales
•	Indispensables :
•	lancer un objet,
•	calculer une trajectoire,
•	afficher le score,
•	détecter une collision.
5.2 Fonctionnalités secondaires
Optionnelles :
•	menu,
•	niveaux,
•	aide,
•	messages éducatifs.
5.3 Découpage des fonctionnalités en tâches
Pour faciliter le développement, chaque fonctionnalité doit être découpée en tâches plus petites. Voici un exemple sous forme de tableau :
Fonctionnalité	Tâches à réaliser
Lancer un objet	1. Créer l’objet projectile (forme, couleur) 2. Définir les paramètres de lancement (vitesse, angle) 3. Calculer la trajectoire parabolique 4. Afficher le projectile en mouvement 5. Détecter collision avec la cible 6. Mettre à jour le score et afficher un message
Calculer une trajectoire	1. Définir les paramètres physiques 2. Implémenter la formule de trajectoire 3. Tester avec différentes valeurs 4. Ajuster pour le rendu à l’écran
Afficher le score	1. Créer une zone d’affichage 2. Mettre à jour le score après chaque réussite 3. Ajouter animations ou feedback visuel
Détecter collision	1. Définir les zones cibles 2. Vérifier position projectile 3. Déclencher événement (score, message)
Menu	1. Créer l’écran de menu 2. Ajouter boutons pour démarrer, options, quitter 3. Tester navigation menu
Niveaux	1. Définir les différents niveaux de difficulté 2. Adapter trajectoires et cibles 3. Tester progression joueur
Aide	1. Créer écran d’aide 2. Ajouter instructions et conseils 3. Vérifier affichage correct
Messages éducatifs	1. Définir messages à afficher 2. Lier messages aux actions du joueur 3. Vérifier affichage au bon moment

Ce découpage permet de :
•	mieux organiser le travail dans l’équipe,
•	répartir les tâches entre les membres,
•	tester chaque sous-partie individuellement.


6. Tests simples
Avant de finaliser votre jeu, vous devez réaliser des tests simples pour vérifier :
•	que la trajectoire se calcule correctement,
•	que les objets se déplacent comme prévu,
•	que les boutons et l’interface répondent,
•	que le score et les messages s’affichent correctement.
6.1 Méthode de test
•	Choisissez une fonctionnalité à tester (ex. lancer de projectile).
•	Définissez des valeurs d’entrée simples (angle, vitesse).
•	Vérifiez que le résultat correspond à vos attentes.
•	Notez les résultats et anomalies dans le carnet de bord.
•	Ces tests sont obligatoires et seront validés par vos tuteurs.

7. Organisation du travail
7.1 Répartition des rôles
•	coordination,    heloise ABEL
•	développement,   lorenzo
•	interface graphique,  antonin
•	tests,      aksil 
•	documentation.   Heloise ABEL


9. Bilan carbone – calculs obligatoires 
– https://chatgpt.com/c/696ed581-82cc-8330-a760-158e59ac3f1f 
1️⃣ Hypothèse de base
•	Jeu très léger (moins de ~2,4 MB) et sans gros calcul graphique. (Back2Gaming)
•	La consommation vient surtout :
o	de l’électricité de l’ordinateur
o	un peu du réseau (pubs, score, etc.)
Un smartphone en usage typique produit environ 63 kg CO₂/an si on l’utilise ~1 h par jour. (Compare the Market)
________________________________________
2️⃣ Conversion par heure
63 kg CO₂/an pour 1 h/jour
1 an = 365 h d’utilisation
➡️ ≈ 170 g CO₂ pour 1 heure d’utilisation du téléphone
Mais Tap’Trash est un jeu très léger, donc l’usage réel peut être plus faible.
On peut raisonnablement estimer :
≈ 50 à 150 g CO₂ par heure de jeu
________________________________________
3️⃣ Par partie de Flappy Bird
Une partie dure souvent 10–30 secondes.
Si on prend 60 g CO₂/h :

60 g / 3600 s ≈ 0.017 g/s

Pour une partie de 20 s :

0.017 \times 20 ≈ 0.34 g

➡️ ≈ 0,3 g de CO₂ par partie
________________________________________
4️⃣ Exemple concret
Action	CO₂
1 partie	~0,3 g
10 parties	~3 g
1 heure de jeu	~50–150 g
________________________________________
✅ Conclusion :
Le bilan carbone de Tap’Trash est extrêmement faible. L’impact vient surtout de posséder et charger le smartphone, pas du jeu lui-même.
