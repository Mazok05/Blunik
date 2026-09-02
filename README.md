# Blunik — Simulateur de régularité

Application web installable (PWA). Une fois installée sur l'iPhone, elle
s'ouvre en plein écran, sans barre d'adresse ni barre d'outils Safari, et
fonctionne entièrement hors ligne — y compris pendant un rallye, sans réseau.

## Contenu du dossier

    index.html              l'application entière (un seul fichier)
    manifest.webmanifest    nom, icône, mode plein écran
    sw.js                   mode hors ligne
    icons/                  icônes d'écran d'accueil
    splash/                 écrans de lancement iPhone
    .nojekyll               nécessaire à GitHub Pages

## Mise en ligne sur GitHub Pages

Tout se fait depuis Safari sur l'iPhone ou depuis un ordinateur, en 5 minutes.

1. Créez un compte sur **github.com** (gratuit).
2. Bouton **+** en haut à droite → **New repository**.
   - Repository name : `blunik`
   - Cochez **Public**
   - **Create repository**
3. Sur la page du dépôt : **uploading an existing file**.
   Déposez **tout le contenu** de ce dossier — `index.html`,
   `manifest.webmanifest`, `sw.js`, `.nojekyll`, et les dossiers `icons`
   et `splash` avec leurs images.
   Puis **Commit changes**.
4. Onglet **Settings** → **Pages** (colonne de gauche).
   - Source : **Deploy from a branch**
   - Branch : **main**, dossier **/ (root)** → **Save**
5. Attendez une à deux minutes. L'adresse s'affiche en haut de la page :

       https://VOTRE-NOM.github.io/blunik/

## Installation sur l'iPhone

1. Ouvrez cette adresse **dans Safari** (pas Chrome : iOS n'autorise que Safari
   à installer une application).
2. Touchez le bouton **Partager** (le carré avec la flèche).
3. Faites défiler et touchez **Sur l'écran d'accueil**.
4. Le nom proposé est **Blunik** → **Ajouter**.

L'icône apparaît sur l'écran d'accueil. Elle s'ouvre en plein écran, avec son
écran de lancement, comme une application de l'App Store.

## Bon à savoir

- **Hors ligne** : au premier lancement l'application se met en mémoire. Ensuite
  elle fonctionne sans réseau. Ouvrez-la une fois chez vous avant le rallye.
- **Écran allumé** : en bas de l'application, le bouton *Écran allumé* empêche
  l'iPhone de s'éteindre pendant une ZR.
- **Carnet de rallye** : les données saisies restent sur l'appareil. Utilisez
  *Exporter* pour en garder une copie.
- **Mise à jour** : redéposez les fichiers sur GitHub, puis changez la ligne
  `const CACHE = 'blunik-v1.2'` de `sw.js` (par exemple en `v1.2`). Sans ce
  changement, les iPhones déjà installés garderont l'ancienne version.
- L'application est indépendante de Blunik Technology et ne remplace pas la
  notice de l'appareil.
