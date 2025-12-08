# **Consignes du projet de jeu : Maze-3D**

*Cette réécriture des consignes a été réalisée par une IA.*

---

## **Mise en situation**

Dans une petite ville appelée **« Arky »**, située quelque part sur la planète, il existe une **réserve constituée de capsules néfastes pour l’environnement**. Ces capsules sont surveillées par d’autres capsules identiques.  

**Arthur**, notre héros, a pour mission de **faire intrusion dans ce village et de détruire le plus grand nombre de capsules néfastes en un temps limité** (exemple : 1 minute).  

Cependant, il doit également **pouvoir s’échapper du labyrinthe** où il est enfermé. Le labyrinthe possède une **seule porte de sortie**. Arthur doit :  
1. Retrouver la clé du labyrinthe.  
2. Ouvrir la porte pour accéder à la réserve.  

Dans ce labyrinthe :  
- Il y a au moins **deux ennemis en mouvement dans chaque corridor**.  
- Arthur dispose de **1 minute** pour trouver la clé, rejoindre la porte et sortir.  
- **Si Arthur est touché par un ennemi ou ne sort pas dans le temps imparti, il meurt.**

---

## **Mandat**

Réaliser un **jeu simulant la situation décrite**.  

---

### **Étape 1 : Écran d’accueil**

- **Play** : accéder au labyrinthe  
- **Exit** : quitter le jeu  

---

### **Étape 2 : Labyrinthe**

- Le labyrinthe doit être **complexe et sans vue sur le ciel**.  
- La **porte de sortie** doit être **visuellement identifiable**.  
- La porte **ne s’ouvre que si Arthur détient la clé** (collision avec la clé).  
- **Éléments à inclure dans le labyrinthe** :  
  - Brouillard  
  - Couleur de fond au choix  
  - La clé (position visible par la caméra)  
  - Des ennemis en mouvement dans les différentes pièces ou corridors  
  - **Compte à rebours** indiquant le temps restant  

**Interactions :**  
- Si Arthur est touché par un ennemi ou si le temps est écoulé : afficher **GameOver**, puis retour à l’écran d’accueil après 1 seconde.  
- Si Arthur sort du labyrinthe : il arrive dans la **réserve de Arky**.  

---

### **Étape 3 : Réserve de Arky**

1. **Environnement** : créer un espace réaliste (montagnes, arbres, végétation, cours d’eau, skybox, etc.)  
2. **Capsules** :  
   - Capsules néfastes et surveillantes réparties **aléatoirement** sur le terrain (ex : espace de [250, 250]).  
   - Au moins **200 capsules néfastes et 200 capsules surveillantes**.  
   - Toutes les capsules sont **visuellement identiques**.  
3. **Actions du héros et des capsules** :  
   - Capsules surveillantes : changent de couleur et attaquent Arthur si ce dernier est à moins de 10 cm, sinon elles reprennent leur couleur initiale.  
   - Capsules néfastes : détruites au contact avec Arthur ; le nombre de capsules détruites augmente et une **particule d’effet** est générée.  
   - Capsules surveillantes : si elles touchent Arthur, il **perd deux capsules** ; une **explosion** est générée, mais la capsule survit.  
4. **Interface** : toujours visible :  
   - Temps restant  
   - Nombre de capsules détruites  

**Fin de partie :**  
- Lorsque le temps est écoulé ou que le nombre de capsules détruites est atteint : afficher **GameOver** et revenir à l’écran d’accueil après 1 seconde.  

---

## **Grille de correction**

**Remise** :  
- Échéance : vendredi 08 novembre 2024, avant 23h59:59  
- Remise sur Léa  
- Présentation en classe : lundi 11 novembre  

**Évaluation :**  

| Catégorie | Détails | Poids |
|-----------|--------|------|
| Menu | Play / Exit | 5% |
| Labyrinthe | Gestion du héros, ennemis, porte, clé, animations, temps | 25% |
| Réserve de Arky | Gestion du héros, capsules surveillantes, capsules néfastes, environnement, animations, pointage, temps | 15% |
| Classes métiers | Découpage et clarté du code, organisation des dossiers (scripts, matériels, prefabs…), respect des consignes | 5% |

**Total : 50%** %
