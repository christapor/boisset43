# CONTEXTE PROJET : BOISSET43.FR

## 1. VISION & OBJECTIFS
* **Quoi :** Site officiel de la commune de Boisset (Haute-Loire).
* **Objectif :** Offrir une vitrine moderne, claire et accessible pour la municipalité.
* **Cibles :** * Les habitants (actus locales, démarches administratives, calendrier des événements, comptes-rendus du conseil).
    * Les touristes et nouveaux arrivants (patrimoine, hébergements, vie associative).
* **Partenaire clé :** Florian, le Maire de Boisset (collaboration directe sur les outils numériques communaux).

## 2. STACK TECHNIQUE
* **Philosophie :** Pas de frameworks lourds, du solide, du léger, du maîtrisable.
* **Front-end :** HTML5, CSS3 (Responsive Design), JavaScript natif (Vanilla JS).
* **Hébergement & Versioning :** GitHub + Vercel (déploiement continu).
* **Back-end / Base de données :** Supabase (authentification, stockage des actus, logs, données dynamiques).
* **Environnement de dev :** MX Linux / Windows Ghost.

## 3. ÉTAT ACTUEL & STABILITÉ
* Le site vitrine de base est fonctionnel et en ligne.
* La structure responsive est en place pour s'adapter aux smartphones (priorité aux téléphones des administrés).
* La connexion avec Supabase est opérationnelle pour la récupération des contenus dynamiques majeurs.

## 4. POINTS SENSIBLES & VIGILANCES
* **Accessibilité (RGAA) :** Le site d'une mairie doit être lisible par tous (contrastes, tailles de police, navigation clavier).
* **Performance :** Chargement rapide même avec une connexion mobile instable dans la Haute-Loire.
* **Gestion du Calendrier / Actus :** Interface simple pour la mise à jour des événements de la commune et des alertes de la mairie.

## 5. DERNIÈRES MODIFS & PROCHAINES ÉTAPES
* *Fait :* Structuration globale et mise en conformité du nom de domaine.
* *En cours :* Optimisation du responsive et liaison propre des tables Supabase pour les actus municipales.
* *À faire :* Finaliser le module d'affichage du calendrier des événements et valider l'accès admin pour la mairie.

********** EDIT DU 27 MAI 2026 **********

# CONTEXTE PROJET : BOISSET43

## 1. VISION & INFOS CLÉS
* **Projet :** Site officiel de la commune de Boisset (Haute-Loire).
* **URL actuelle :** boisset43.vercel.app (future : boisset43.fr)
* **Cibles :** Habitants (dont séniors), touristes, nouveaux arrivants.
* **Stack :** Full Vanilla (HTML5, CSS3, JS natif), GitHub, Vercel (déploiement continu), Supabase (Auth, DB pour actus et alertes).
* **Design :** Responsive, clair, forts contrastes. Menu "hamburger" cliquable sur mobile. Grand espace (450px) en haut et en bas de page pour laisser respirer l'image de fond (`fond.jpeg`).

## 2. STRUCTURE DES PAGES (Récemment mises à jour)
Toutes les pages partagent la même structure globale (header, sub-header, footer, espaces parallax).

* **index.html :** 
  - Accueil. 
  - Intègre une section dynamique Supabase pour les actus.
  - Alerte Mairie (rouge) gérée en JS (`mairie.boisset@orange.fr`).
* **mairie.html :** 
  - Horaires (Lundi, Mardi, Jeudi, Samedi. Fermé Mercredi et Vendredi).
  - Trombinoscope équipe municipale (Florian Capdevielle, Eric Gagnère, Denise Boutin, Murielle Bouillon, Cédric Dérail, Thierry Petit).
  - Alerte Mairie (rouge) en double avec l'accueil.
* **services.html :** 
  - Infos CCAS, École, Santé (Dr Rodriguez, Pharmacie Pérez-Desbrun).
  - Intégration Syndicat des eaux (SGEV) avec logo cliquable.
* **territoire.html :** 
  - Histoire, patrimoine, tourisme (structure prête, contenu en attente).
* **vie-locale.html :** 
  - Annuaire complet (39 cartes : 19 Assos, 6 Commerces, 14 Entreprises).
  - Barre de recherche dynamique (JS) placée *avant* les associations avec un texte explicatif adapté aux séniors. Le JS filtre sur le `.textContent` global sans tenir compte de la casse ou des accents.
* **login.html / edit.html :** 
  - Espace pro (Magic Link Supabase). 

## 3. PROCHAINES ÉTAPES (To-Do)
* Mettre en place l'édition des fiches (login/edit) directement depuis la page `vie-locale.html` pour que les 39 artisans/assos puissent modifier leurs infos eux-mêmes (en attente de leurs adresses email).
* Nettoyer `index.html` pour supprimer les cartes en double (qui sont maintenant proprement classées dans `vie-locale.html`).
* Intégrer les photos manquantes (agents, élus).

## 4. DIRECTIVES POUR L'ASSISTANT (CHRIS DEV)
* Ton direct, technique, pas de politesses inutiles. Tutoiement.
* Si modification de code, donner le nom du fichier et utiliser des "snippets" (morceaux de code) avec indication claire de "couper entre la ligne X et Y" pour économiser des tokens, SAUF si le fichier est court ou demande une refonte complète.

