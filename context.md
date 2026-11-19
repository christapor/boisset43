# CONTEXTE PROJET : BOISSET43.FR

## 1. VISION & OBJECTIFS
* **Quoi :** Site officiel de la commune de Boisset (43500, Haute-Loire).
* **URL actuelle :** `boisset43.vercel.app` (bascule finale prévue sur `boisset43.fr` via hébergement souverain français LWS).
* **Objectif :** Offrir une vitrine moderne, sobre numériquement, accessible et 100 % conforme au RGPD pour la municipalité.
* **Cibles :**
  * Les habitants (actus locales, démarches administratives, calendrier des événements, comptes-rendus du conseil, alertes mairie, boîte à idées).
  * Les touristes et nouveaux arrivants (histoire, patrimoine, randonnées, hébergements, bonnes tables, vie associative).
* **Partenaires clés :** Florian Capdevielle (Maire de Boisset) et Éric (Premier Adjoint), en collaboration avec TaporDigital (Chris TAPOR).

## 2. STACK TECHNIQUE & SOUVERAINETÉ RGPD
* **Philosophie :** Full Vanilla — zéro framework lourd, zéro cookie traceur publicitaire, zéro dépendance GAFAM.
* **Front-end :** HTML5, CSS3 (Responsive Design, variables `--azur`, `--sinople`, `--argent`, `--dark`), JavaScript natif (Vanilla JS), Font Awesome 6.5.1, Google Fonts (`Amatic SC`).
* **Hébergement & Versioning :** GitHub (`christapor/boisset43`) + Vercel (préproduction/CI) → cible finale LWS (France).
* **Back-end / Base de données :** Supabase (authentification Magic Link, stockage des actus, alertes mairie, données dynamiques).
* **Formulaires (Boîte à idées) :** Formward (infrastructure 100 % UE : Hostup AB Suède + Mailjet France), hachage IP HMAC-SHA-256, rétention automatique 30 jours, honeypot `_gotcha`, validation serveur `_consent` et DPA Article 28 RGPD v1.2 signé le 19/11/2026.
* **Cartographie & Réseaux sociaux :**
  * Google Maps remplacé par **OpenStreetMap** centré sur la Mairie (`45.323649, 3.982670`), sans traceurs.
  * SDK Facebook/Meta supprimé et remplacé par un lien direct protégé par une modale **sas de sortie RGPD** (`#fb-rgpd-modal` / `openFbModal()`).
* **Environnement de dev :** MX Linux / Windows 11.

## 3. STRUCTURE DES PAGES (État au 19 novembre 2026)
Toutes les pages partagent la même architecture harmonisée (header fixe, sub-header épuré à 5 entrées sans menus déroulants : `Accueil | Mairie | Services | Activités | Vie locale`, logo blason fixe, espaces parallax de 450px, bouton retour en haut, footer RGPD).

* **`index.html` :**
  * Page d'accueil avec flux dynamique Supabase pour les actualités et alerte mairie rouge (`mairie.boisset@orange.fr`).
  * Intégration Illiwap, bloc Facebook avec sas de sortie RGPD (`openFbModal()`), carte OpenStreetMap de la mairie et formulaire Boîte à Idées connecté à Formward.
  * Navigation sub-header harmonisée (suppression des anciens menus déroulants).
* **`mairie.html` :**
  * Horaires d'ouverture (Lundi, Mardi, Jeudi, Samedi ; fermé Mercredi et Vendredi).
  * Trombinoscope de l'équipe municipale (Florian Capdevielle, Eric Gagnère, Denise Boutin, Murielle Bouillon, Cédric Dérail, Thierry Petit).
  * Alerte mairie synchronisée avec l'accueil.
* **`services.html` :**
  * Écoles (Mélanie Perbet, Thiphaine Jalabert, Arnaud Beurion).
  * **CCAS :** présentation + bouton vers la fiche officielle `service-public.gouv.fr`.
  * **Santé & Numéros utiles :** Dr Anaïs Rodriguez, Pharmacie Pérez-Desbrun, Urgences (`15 / 112 / 18`).
  * **Eau & Assainissement :** Syndicat de Gestion des Eaux du Velay (`sgev.fr`).
  * **Déchets :** collecte CC Marches du Velay Rochebaron (`04 71 61 74 34`), traitement SYMPTTOM (`04 71 75 57 57`), horaires hiver/été de la déchetterie de Saint-Pal-de-Chalencon (Trespeyres) et liens officiels.
* **`activites.html` (remplace l'ancien `territoire.html`) :**
  * **Histoire :** toponymie (*Boschetum*
