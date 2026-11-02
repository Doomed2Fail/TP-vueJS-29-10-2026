# TP Vue.js — 29/10/2026

Travaux pratiques réalisés par ER-RAFIY Taha Amine et SAADEDDINE Zineb. Le dépôt regroupe trois applications indépendantes développées avec Vue 3 et Vite.

## Projets

| TP | Projet | Notions abordées |
| --- | --- | --- |
| [TP 3](TP-ERRAFIY%26SAADEDDINE/TP-3-Composants-Cycle-de-vie/) | Catalogue de livres | Composants, props, événements, slots et cycle de vie |
| [TP 4](TP-ERRAFIY%26SAADEDDINE/TP%204%E2%80%93%20Router_Composition%20API/starter/) | Catalogue de livres avec navigation | Vue Router, Composition API et état partagé réactif |
| [TP 5](TP-ERRAFIY%26SAADEDDINE/TP-5-Jobs-App/) | Gestion d'offres d'emploi | Vue Router, appels HTTP et API REST simulée |

## Prérequis

- Git, pour cloner le dépôt.
- Node.js 18 ou une version plus récente compatible avec Vite 6, et npm.
- Un navigateur récent.

```sh
git clone https://github.com/Doomed2Fail/TP-vueJS-29-10-2026.git
cd TP-vueJS-29-10-2026
```

Chaque TP possède son propre `package.json` : installez les dépendances dans le dossier de l'application à utiliser. Les commandes ci-dessous partent de la racine du dépôt. Suivez ensuite l'adresse affichée par Vite dans le terminal.

## TP 3 — Composants et cycle de vie

Le catalogue permet d'ajouter des livres et de les marquer comme favoris. Il illustre la communication entre composants, les slots, un chargement initial simulé et le focus automatique du formulaire. Les données sont conservées en mémoire et réinitialisées au rechargement.

```sh
cd "TP-ERRAFIY&SAADEDDINE/TP-3-Composants-Cycle-de-vie"
npm ci
npm run dev
```

## TP 4 — Router et Composition API

Cette version du catalogue ajoute une navigation entre la liste et la fiche d'un livre, une page pour les adresses inconnues et un état partagé avec `reactive()`. Le chargement est simulé et les données sont conservées en mémoire.

```sh
cd "TP-ERRAFIY&SAADEDDINE/TP 4– Router_Composition API/starter"
npm ci
npm run dev
```

Routes principales : `/` pour le catalogue et `/livre/:id` pour le détail d'un livre.

## TP 5 — Jobs App

L'application permet de consulter et filtrer les offres par type de contrat, d'afficher leur détail, d'en ajouter, de les modifier et de les supprimer. Elle utilise JSON Server comme API locale ; les données sont enregistrées dans `db.json`.

Dans un premier terminal, depuis la racine du dépôt :

```sh
cd "TP-ERRAFIY&SAADEDDINE/TP-5-Jobs-App"
npm ci
npm run api
```

Dans un second terminal, depuis la racine du dépôt :

```sh
cd "TP-ERRAFIY&SAADEDDINE/TP-5-Jobs-App"
npm run dev
```

L'API doit rester active sur `http://localhost:3000/jobs` pendant l'utilisation de l'application. Le port 3000 doit être disponible. Les modifications effectuées depuis l'application modifient `db.json` ; pour retrouver les données initiales, restaurez ce fichier depuis Git si vous n'avez pas de modifications à conserver.

Routes principales : `/` (liste), `/add` (ajout), `/jobs/:id` (détail) et `/jobs/:id/edit` (modification).

## Compilation et aperçu

Dans le dossier du TP concerné, après installation :

```sh
npm run build
npm run preview
```

La compilation produit le dossier `dist/` ; `preview` permet de vérifier localement cette version compilée. Pour le TP 5, l'API doit également être lancée avec `npm run api`.

## Organisation

```text
TP-ERRAFIY&SAADEDDINE/
├── TP-3-Composants-Cycle-de-vie/
├── TP 4– Router_Composition API/
│   └── starter/
└── TP-5-Jobs-App/
    ├── db.json
    └── src/
        ├── components/
        ├── router/
        ├── services/
        └── views/
```

Chaque application contient notamment `src/`, `package.json`, `package-lock.json` et `vite.config.js`.
