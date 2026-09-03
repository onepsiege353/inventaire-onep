# ONEP — Application d'Inventaire des Immobilisations (version PRO 7.7)

**Fichier : `ONEP_Inventaire_Pro_v7.html`** (nom versionné — indispensable pour éviter toute ancienne copie en cache ; il y a aussi `ONEP_Inventaire_Pro.html`, identique) — une seule application HTML, **100 % autonome, hors-ligne et sécurisée**.
Tout est intégré dans le fichier : le logo ONEP, les 853 biens du Fichier 2026, le plan d'amortissement
(128 biens), les bibliothèques Excel (SheetJS) et PDF (jsPDF), le générateur de QR codes, la page de
connexion et le moteur complet d'inventaire. Le code source est **masqué** (données encodées, commentaires
supprimés) pour un fichier propre et professionnel.

> ✅ **Aucune connexion internet n'est requise** : le fichier fonctionne sur PC, tablette et smartphone,
> ouvert directement depuis le disque ou téléchargé.

---

## 1. 🔐 Connexion (nouveau)

À l'ouverture, une **page de connexion** élégante aux couleurs de l'ONEP s'affiche.

**Comptes par défaut** (à modifier dans ⚙️ Paramètres → Comptes & utilisateurs) :

| Rôle | Identifiant | Mot de passe | Droits |
|------|-------------|--------------|--------|
| **Administrateur** | `admin` | `onep2026` | Tout : paramètres, comptes, audit, distribution |
| **Agent d'inventaire** | `agent` | `inventaire2026` | Saisie terrain, fiches, rapports (sans paramètres) |

- ✅ « Rester connecté sur ce poste » : session conservée 7 jours (sinon session de navigation).
- 🔒 Mot de passe masquable (œil 👁).
- 👥 **Gestion des comptes** dans ⚙️ Paramètres : ajouter un agent (identifiant, nom, rôle),
  changer un mot de passe, supprimer un compte. Impossible de supprimer le dernier administrateur
  ou le compte connecté.
- 🚪 **Déconnexion** : bouton dans l'en-tête (le journal d'audit trace chaque connexion/déconnexion).
- 🛡️ Les agents **ne voient pas** les onglets Paramètres et Audit (accès réservé administrateur).

---

## 2. ✨ Nouveau design (refonte complète)

Interface refondue aux **couleurs officielles de l'ONEP** (bleu océan / navy / cyan) et inspirée des
meilleures applications d'inventaire (Snipe-IT, AssetTiger) :

- **Logo ONEP** intégré dans l'en-tête, la page de connexion et le favicon (aucun fichier externe).
- **Bannière d'accueil** sur le tableau de bord : message personnalisé, actions rapides
  (Lancer l'inventaire, Nouvelle fiche, Étiquettes QR) et **jauge de progression** de l'inventaire.
- **Recherche globale** dans l'en-tête : tapez un mot-clé + Entrée → résultat multi-source instantané.
- Cartes KPI avec accents colorés, graphiques (états + top directions), tableaux, boutons,
  formulaires et badges entièrement redessinés.
- Fond animé de la connexion (vagues, halos) + micro-animations (cartes, boutons, barre de progression).


---

## 2 bis. 🚀 Améliorations de la version 4.0

| # | Amélioration | Détail |
|---|--------------|--------|
| 1 | 📈 **Métriques corrigées** | Le « taux de réalisation inventaire » du tableau de bord reflète désormais la **vraie couverture** (biens retrouvés / référentiel), et le compteur « biens affectés projets » utilise les projets réels. |
| 2 | 🔀 **Tri des tableaux** | Cliquez sur les en-têtes de la liste des immobilisations pour trier (n° fiche, désignation, direction, état, valeur…). |
| 3 | 👁 **Fiche détaillée** | Bouton « Voir » sur chaque ligne : fiche complète (photo, QR, comptes, projets, mouvements récents, remarques) + boutons Imprimer / Modifier. |
| 4 | 📄 **Fiches d'inventaire papier** | Onglet Inventaire : générez des **feuilles de pointage imprimables par direction** (cases à cocher Bon/Défectueux/Abîmé/Manquant, signatures agent/détenteur/coordinateur) — parfait quand un agent n'a pas de tablette. |
| 5 | 📥 **Import Excel en masse** | Onglet Immobilisations : téléchargez le **modèle Excel**, remplissez-le, importez-le → les fiches sont créées automatiquement (véhicules détectés via le compte 245110, états normalisés, doublons ignorés). |
| 6 | 📤 **Export CSV** | Export rapide de la liste en CSV (tableur universel). |
| 7 | 📷 **Photos des biens** | Attachez une photo à chaque fiche (compressée automatiquement, stockée dans le fichier de données). |
| 8 | ⚠️ **Alertes intelligentes** | Points d'attention sur le tableau de bord : biens entièrement amortis, disparus/volés, à réformer, à suivre (< seuil), sans détenteur — cliquez pour filtrer. |
| 9 | 📊 **Graphiques supplémentaires** | Répartition par compte comptable + acquisitions par année. |
| 10 | 🖼️ **Logo sur les PDF** | Les rapports PDF générés portent désormais le logo ONEP en en-tête. |
| 11 | ⌨️ **Raccourcis** | `Ctrl+K` (ou `Cmd+K`) : focus sur la recherche globale · `Échap` : ferme la fiche détaillée. |
| 12 | 🛠️ **Pré-remplissage affiné** | Créer une fiche depuis le Fichier 2026 / plan d'amortissement recalcule automatiquement la valeur nette et les champs véhicule. |


## 2 ter. 🖨️ & 🎨 Mises à jour de la version 5.0

- **Nouveau logo ONEP officiel (HD)** : votre logo en bannière (issu du PDF) est intégré en haute
  définition dans l'en-tête, la page de connexion, le favicon et les rapports PDF (avec le bon
  format largeur/hauteur).
- **Impression des étiquettes corrigée** : l'impression passe désormais par une **fenêtre
  d'impression dédiée (iframe)** avec un format **A4 exact** — plus de pages blanches ni de
  contenu décalé. Les étiquettes (12 ou 24 par page) s'alignent parfaitement sur la page, avec
  des **QR codes haute résolution** pour un scan fiable après impression.
- Les **fiches d'inventaire papier** et les **fiches individuelles** utilisent le même moteur
  d'impression A4 professionnel.

**Conseil d'impression :** choisissez « Étiquettes » dans l'onglet 🏷️, réglez la densité
(12/page recommandé pour des QR bien lisibles), puis « Imprimer les étiquettes » — la boîte de
dialogue d'impression du navigateur s'ouvre sur les étiquettes uniquement (marges minimales, échelle 100 %).


## 2 quater. 🏷️ Étiquettes — nouveautés de la version 6.0

- **🖨️ Impression de toutes les étiquettes d'un coup** : le bouton « Imprimer TOUTES les étiquettes »
  génère l'intégralité des étiquettes (référentiel complet + fiches) en une seule impression.
- **📐 Format paysage A4 (par défaut)** : les étiquettes s'impriment en grand format paysage
  (4 colonnes × 3 rangées pour 12/page, ou 6×4 pour 24/page) — QR codes et textes bien lisibles.
  Le portrait reste disponible si vous préférez.
- **⚡ Étiquette automatique à la création d'une fiche** : dès qu'un bien est enregistré dans
  l'onglet Immobilisations (nouveau n° de fiche), son étiquette est créée automatiquement et
  retrouvable dans l'onglet 🏷️ Étiquettes (source « Fiches créées » + filtre par code).
  La modification d'une fiche met à jour son étiquette ; la suppression la retire.
- **⛔ Anti-doublon des codes** : un code déjà utilisé (fiche, étiquette ou référentiel BS-/ONEP-)
  est **bloqué** — à la création d'une fiche (message « Code déjà utilisé — impossible ») et dans
  le formulaire « Créer une étiquette manuellement » (validation en temps réel, bouton désactivé).
- **➕ Création manuelle d'étiquette** : ajoutez une étiquette indépendante (code unique) en 1 clic.
- **🔎 Source « Toutes »** : fiches + référentiel, triées par code.


## 2 quinque. 🔧 Mises à jour de la version 7.0

- **📐 Étiquettes auto-adaptatives au papier A4** : plus aucun débordement. Les grilles utilisent des
  colonnes `minmax(0,1fr)` (le contenu ne peut pas élargir une colonne) et des **hauteurs fixes en
  millimètres** par format (65 mm en paysage 12/page, 48 mm en paysage 24/page…). La désignation est
  limitée à 2 lignes (clamp), le code tronqué avec « … », et tout excédent est masqué proprement.
  L'aperçu à l'écran reflète exactement le résultat imprimé.
- **🏢 Fiche d'inventaire papier : toutes les directions** : le menu déroulant affiche désormais les
  **16 directions officielles de l'ONEP** (+ celles ajoutées dans les fiches), au lieu des 5
  premières seulement.
- **🔎 Recherche par nom du détenteur** : dans « Scanner ou saisir le code du bien », tapez le nom
  du détenteur (ex. KOUAKOU, KOUAME, ABGROU) → la liste des biens correspondants s'affiche, cliquez
  pour ouvrir la fiche. La recherche couvre désormais : code, désignation, **détenteur** et service.







### 2 undecies. 👤 Version 7.7 — Remise à zéro accessible en mode agent

- **En mode agent**, l'onglet ⚙️ **Paramètres** n'est plus bloqué : il s'ouvre désormais en
  **vue réduite** avec une bande d'information « Mode agent — accès limité ».
- L'agent y trouve la **💾 Sauvegarde complète** et l'encart **🧹 Repartir avec un fichier
  vierge** (double confirmation puis retour à l'écran de connexion, données d'exemple bloquées).
- Les sections réservées à l'administrateur (**configuration de l'organisation**, **comptes &
  utilisateurs**, **distribution**) restent **masquées pour les agents** et réapparaissent
  automatiquement lors d'une connexion admin (droits recalculés à chaque connexion/déconnexion).

### 2 decies. 🧹 Version 7.6 — Repartir avec un fichier vierge

- **Option « Repartir avec un fichier vierge »** dans l'onglet ⚙️ Paramètres → « Données &
  sauvegardes » : un encart dédié (fond jaune) explique l'action.
- **Tout est supprimé en une fois** : fiches d'immobilisations et étiquettes, projets et biens
  affectés, mouvements, localisations, sessions d'inventaire, audit, paramètres personnalisés,
  utilisateurs créés et sessions ouvertes.
- **Les données d'exemple ne reviennent plus** : contrairement à une simple suppression des
  champs, un verrou interne empêche les fiches/projets/mouvements de démonstration de se
  recréer aux démarrages suivants. Le fichier reste vierge durablement.
- **Comptes par défaut restaurés** : après la réinitialisation, reconnectez-vous avec
  `admin` / `onep2026` (ou `agent` / `inventaire2026`).
- **Sécurité** : deux confirmations sont demandées (l'action est irréversible) ; il est conseillé
  de faire d'abord une **sauvegarde complète (.json)** pour conserver un historique.

### 2 nonies. 📱💻 Version 7.5 — Application responsive (téléphone & tablette)

- **🍔 Menu hamburger sur mobile** : sur écran de moins de 900 px, la barre de navigation se
  range dans un **tiroir latéral** élégant (logo ONEP, tous les onglets, recherche globale,
  profil de l'agent, déconnexion). Bouton **☰** en haut à droite ; fermeture par ✕, clic
  à l'extérieur, clic sur un lien, ou touche Échap.
- **📐 Adaptation automatique** à toutes les tailles d'écran :
  - **Tablette (≤ 1100 px)** : espacements et cartes compactés ;
  - **Mobile (≤ 900 px)** : menu tiroir, graphiques sur 1 colonne ;
  - **Petit mobile (≤ 640 px)** : cartes KPI sur 2 colonnes, formulaires sur 1 colonne,
    en-tête réduit (sous-titre masqué), boutons et héro empilés, tableaux plus lisibles
    (défilement horizontal fluide), champs de saisie agrandis à 16 px (pas de zoom
    automatique iOS au clic), page de connexion et fenêtres modales adaptées.
- **🔎 Recherche globale fonctionnelle partout** : depuis le tiroir mobile comme depuis le
  desktop, tapez un mot-clé + Entrée → la conciliation s'ouvre avec les résultats.
- Aucun redimensionnement manuel requis : l'application s'adapte seule, y compris lors de la
  rotation de l'appareil.

### 2 octies. 🔄 Version 7.4 — Mouvements : suppression d'un mouvement enregistré

- **🗑️ Supprimer un mouvement** : chaque ligne de l'historique des mouvements (onglet
  « Mouvements ») dispose maintenant d'un bouton **corbeille** dans une nouvelle colonne
  « Actions ». Une confirmation est demandée avant suppression.
- Le tableau se met à jour immédiatement après suppression.

### 2 septies. 📱 Version 7.3 — QR Code professionnel (logo ONEP + infos du bien)

- **🔍 Au scan, les informations complètes s'affichent** : le QR code n'encode plus seulement le
  numéro de fiche, mais un **bloc d'informations professionnel** : « ONEP — Office National de
  l'Eau Potable », **Bien N°**, **désignation**, **détenteur**, **direction** et **service**.
  Un simple scan avec l'appareil photo du téléphone affiche tout cela proprement.
- **🎨 QR code élégant** : le logo ONEP est **intégré au centre** du QR (correction d'erreur
  élevée pour rester scannable), modules bleu ONEP, bordure et marges propres.
- **🏷️ Étiquettes repensées** : bandeau « ONEP — Office National de l'Eau Potable · Inventaire
  2026 » en tête de chaque étiquette, puis QR avec logo, n° de fiche, désignation, détenteur et
  direction.
- **📋 Onglet « Générer QR Code »** : aperçu professionnel (carte ONEP avec QR, désignation,
  détenteur, direction, service) + bouton **« Télécharger PNG »**. Si vous saisissez un n° de
  fiche ou un code connu (BS-…, ONEP-…), les informations du bien sont ajoutées automatiquement.
- **🔎 Scan dans l'application** : scanner un QR d'étiquette (fiche ou référentiel) remplit
  automatiquement la recherche — le code est extrait du QR, et pour les fiches une carte
  professionnelle (désignation, détenteur, direction, valeur) s'affiche directement.
- **🖨️ Fiche d'immobilisation imprimée** : le QR de la fiche contient aussi les informations du
  bien et est plus grand (24 mm) avec le logo ONEP.

### 2 sexies. 🏗️ Version 7.2 — Projets : suppression des biens et stat corrigée

- **🗑️ Retirer un bien d'un projet** : dans « Projets », cliquez **👁️ Visualiser** → chaque bien
  a maintenant un bouton **« Retirer »**. Le bien est retiré du projet (sa fiche d'immobilisation
  reste intacte) et le compteur se met à jour immédiatement.
- **🗑️ Supprimer un projet** : une corbeille est disponible dans la colonne « Actions » de la
  liste des projets (confirmation demandée ; les fiches des biens restent intactes).
- **📊 Statistique « Biens affectés projets » corrigée** : elle compte désormais les biens
  **réellement affectés** dans l'onglet Projets (et non plus les fiches dont le champ
  « Remarques » contenait le mot « projet » — c'était la cause du compteur qui restait bloqué
  sur 1). Elle se recalcule automatiquement après chaque retrait, suppression de projet ou
  suppression de fiche.
- **🧹 Nettoyage automatique** : si une fiche d'immobilisation est supprimée alors qu'elle était
  affectée à un projet, sa référence est automatiquement retirée du projet (plus de « fantôme »
  ni de compteur bloqué).

### 2 quinquies. 🧱 Version 7.1 (anti-débordement garanti)

- **Pages d'impression verrouillées** : chaque page d'étiquettes a maintenant une **hauteur exacte
  (mm)** égale à la zone imprimable A4 (marges de 5 mm retirées) + `overflow:hidden` + page
  insécable → **aucun débordement, même avec des désignations très longues** ou en cas d'arrondis.
  Valeurs : paysage 12/page = 200 mm · paysage 24/page = 199,5 mm · portrait 12/page = 283,5 mm ·
  portrait 24/page = 282,5 mm.
- **Version affichée « 7.8 Pro »** dans le pied de page et l'écran de connexion : vérifiez-la pour
  être certain d'utiliser la dernière version.
- **Toutes les étiquettes** sont imprimées d'un coup (938 biens du référentiel = 79 pages en
  paysage 12/page, dernière page partielle : normal).

---

## 3. Les 12 onglets de l'application

1. **📊 Tableau de bord** — bannière + KPI + répartitions + graphiques.
2. **📋 Immobilisations** — fiches (ajout/modification/suppression), étiquettes de localisation, QR codes.
3. **📂 Fichier 2026** — les 853 biens comptables (codes BS-) : recherche, export, pré-remplissage 1 clic.
4. **📉 Plan amort.** — les 128 biens du plan d'amortissement : dotations, VNC, intégration en fiche.
5. **🔗 Concilier** — recherche multi-source + répartition par compte comptable.
6. **🔍 Inventaire physique** — scan/saisie du code → Retrouvé / Disparu ; sessions exportables et fusionnables.
7. **🏗️ Projets** — immobilisations affectées aux projets.
8. **🔄 Mouvements** — transferts, prêts, réparations, réformes, sorties.
9. **📑 Rapports** — général, direction, service, écarts, mouvements, réformes, clôture → PDF/Excel réels.
10. **🏷️ Étiquettes** — QR codes imprimables (12/24 par page A4).
11. **🕵️ Audit** — journal de traçabilité (500 dernières actions, exportable).
12. **⚙️ Paramètres** — organisation, campagne, seuils + **Comptes & utilisateurs** + sauvegardes + téléchargement agent.

---

## 4. Mode d'emploi — Agents d'inventaire

1. **Télécharger l'application** : lien hébergé ou fichier reçu (e-mail / clé USB), puis onglet
   ⚙️ Paramètres → « Télécharger l'application » pour récupérer le fichier unique.
2. **Ouvrir** le fichier dans un navigateur (aucune installation, aucun accès internet).
3. **Se connecter** avec son compte (l'administrateur crée les comptes agents).
4. **Inventaire physique** : votre nom est pré-rempli → scanner ou taper le code (`BS-001935` ou `ONEP-000174`)
   → choisir l'état observé → **✅ Retrouvé** ou **❌ Disparu**.
5. En fin de journée : **💾 Exporter ma session (.json)**.
6. Le **coordinateur** fusionne les sessions (🔗 Fusionner sessions agents) puis exporte l'inventaire complet.
7. La progression est **sauvegardée automatiquement** dans le navigateur.

---

## 5. Données & sauvegardes

- **💾 Sauvegarde complète (.json)** — exporte tout (fiches, projets, mouvements, sessions, audit, comptes).
- **📂 Restaurer une sauvegarde** — réimporte un fichier précédent.
- **📂 Importer JSON agent(s)** — sur le tableau de bord : fusionne les fiches journalières.
- **🧹 Réinitialiser** — repart de zéro (prudence).

---

## 6. Masquage du code (travail propre)

- Les **données du référentiel (690 Ko)** sont **encodées** dans le fichier et reconstruites à
  l'exécution — plus aucune liste de biens lisible dans le source.
- Les **commentaires de code** sont supprimés par un parseur JavaScript professionnel (acorn),
  sans jamais altérer le fonctionnement (validé par 36 tests automatisés).
- Les bibliothèques (Excel, PDF, QR) sont intégrées : aucun appel réseau.

---

## 7. 🌍 Hébergement en ligne (téléchargement par les agents)

L'application est publiée sur **GitHub Pages** (hébergement gratuit et permanent) :

- **Page de téléchargement** : https://onepsiege353.github.io/inventaire-onep/
- **Fichier application direct** : https://onepsiege353.github.io/inventaire-onep/inventaire-onep.html
- **Dépôt source** : https://github.com/onepsiege353/inventaire-onep

Chaque agent peut ouvrir la page et cliquer **⬇️ Télécharger** pour obtenir le fichier unique
`inventaire-onep.html`, utilisable **hors-ligne** sur PC, tablette ou smartphone.

> **Mise à jour du site** : quand une nouvelle version de l'application est produite, il suffit de
> remplacer le fichier `inventaire-onep.html` dans le dépôt GitHub (branche `main`) — GitHub Pages
> publie automatiquement la nouvelle version en 1 à 2 minutes.

## 8. Fichiers fournis
| Fichier | Rôle |
|---------|------|
| `ONEP_Inventaire_Pro.html` | **L'application** (livrable principal, ~2,0 Mo) |
| `GUIDE_UTILISATION.md` | Ce guide |

*Dossier `_construction/` : éléments techniques du build (bibliothèques, parseur acorn, scripts) — utile uniquement pour régénérer l'application.*

---

*ONEP — Inventaire des Immobilisations · Cahier des charges 2026 · Application autonome 7.8 Pro*

## 9. 🌐 Version 7.8 — Synchronisation en ligne (temps réel)

Depuis la version **7.8 Pro**, l'application peut envoyer **automatiquement** les données saisies par
chaque agent (fiches immobilisations, projets, mouvements, localisations) vers une **base en ligne
sécurisée** (Firebase Realtime Database). L'administrateur dispose alors d'une **vue globale en temps
réel** de toutes les données de tous les agents, sans attendre la fin de la campagne.

### Comment ça marche
1. Chaque appareil (agent ou admin) ouvre l'application **connecté à internet** au moins une fois.
2. Les enregistrements créés ou modifiés sont poussés automatiquement (identifiés par l'agent : nom, poste, horodatage).
3. Sans réseau, l'application fonctionne normalement : les saisies sont **mises en file d'attente** puis
   remontent dès que la connexion revient. Rien n'est perdu.
4. L'administrateur ouvre la **console admin** (page `console.html` sur le site) pour voir, corriger ou
   supprimer n'importe quel enregistrement, et exporter (CSV / JSON).

### Activation sur un poste
**Paramètres → Synchronisation en ligne** (réservé à l'administrateur) :
- **Tester la connexion** : vérifie l'accès à la base ;
- **Envoyer tout l'existant** : à faire une fois après la mise à niveau pour faire remonter les données
  déjà saisies avant la version 7.8 ;
- un point coloré dans l'en-tête indique l'état (🟢 à jour, 🟠 en attente, ⚪ en veille).

### Mise en service de la base (une seule fois, par l'administrateur technique)
1. Dans la console Firebase → **Realtime Database → Règles**, coller le contenu du fichier
   `REGLES_FIREBASE_ONEP.json` fourni avec ce guide, puis **Publier**.
2. Ouvrir `console.html`, se connecter avec `admin@inventaire-onep.local` et le mot de passe choisi
   (le compte est créé automatiquement au premier accès). La console déclare ensuite ce compte comme
   administrateur de la base.

> 🔒 Règles de sécurité : chaque appareil anonyme ne peut écrire que **ses propres données** ;
> seul le compte `admin@inventaire-onep.local` peut tout lire, corriger et supprimer.

### 📊 Inventaire physique en ligne (console admin)

L'onglet **« 🛰️ Inventaire physique »** de la console admin agrège en temps réel les sessions
envoyées par tous les postes d'agents et affiche :

- **Biens attendus** (référentiel Fichier 2026 + plan d'amortissement) ;
- **✅ Retrouvés** et **❌ Disparus** (dédoublonnés : un bien retrouvé par deux postes ne compte qu'une
  fois — le statut « retrouvé » prime sur « disparu », comme dans la fusion locale) ;
- **⏳ Non répertoriés** = biens attendus ni retrouvés ni signalés disparus ;
- **Taux de couverture** = retrouvés / attendus ;
- la **liste détaillée** de chaque statut : code du bien, désignation, compte, famille, agent(s),
  localisation, détenteur, date du relevé, observation, valeur brute et VNC ;
- une **session par poste** listée avec ses compteurs (modifiable ou supprimable) ;
- export **Excel (.xlsx)** : feuille « Synthèse » (indicateurs) + feuille « Détail des biens » (codes détaillés),
  et export CSV du filtre en cours.

### Limites actuelles (version 7.8)
- La base de référence (Fichier 2026 / plan d'amortissement) est identique partout et **n'est pas** synchronisée.
- La console affiche la **dernière version** de chaque fiche en cas de doublon entre postes (les doublons
  sont signalés et peuvent être supprimés par l'administrateur).

---
