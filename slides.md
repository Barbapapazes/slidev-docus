---
theme: aneo
title: Docus pour notre documentation
author: Estéban Soubiran
highlighter: shiki
layout: cover
background: https://images.unsplash.com/photo-1590595154932-1282d8330b46?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1228&q=80
hideInToc: true
---

---
layout: toc
hideInToc: true
---

# Sommaire

<Toc maxDepth="1"/>

---
layout: section
background: https://images.unsplash.com/flagged/photo-1553459706-6bec09533b13?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80
---

# Docus

---
seeMore:
  text: "Documentation"
  href: https://docus.dev/
---

## Qu'est-ce que Docus ?

- Outil de documentation
  - Utilise du [Markdown](https://markdownguide.org/) et du [MDC](https://content.nuxtjs.org/guide/writing/mdc)
  - Génère du HTML
  - Se déploie sur [GitHub Pages](https://pages.github.com/)
- Passe à l'échelle
  - Capable de générer de grosses documentations
- Outil open-source
  - Basé sur Nuxt

<div class="w-40 absolute left-8 bottom-24">
  <LogoDocus/>
</div>
---
seeMore:
  text: "En savoir plus"
  href: https://aneoconsulting.github.io/armonik-docs-theme/guide#a-lot-of-docs
---

## Pourquoi ?

- Facilité de mise en place
  - Facile à installer
  - Facile à configurer
  - Facile à entretenir
- Facilité d'utilisation
  - Pour les développeurs
  - Pour les utilisateurs
- Possibilité de créer des thèmes (essentiel avec nos 10 repositories)

<Alert color="blue" class="mt-4" title="Expérience Développeur">
Docus est rapide, simple et efficace. Il permet de créer une documentation de qualité en un temps record.
</Alert>

---
layout: section
background: https://images.unsplash.com/photo-1596194073132-2524353974f3?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1091&q=80
---

# Mise en place

---

## Installation

- Avoir [Node.js](https://nodejs.org/en/) installé
- Créer un nouveau projet

```bash	
npx nuxi@latest init <folder-name> -t themes/docus

cd <folder-name>
npm install # Install dependencies
npm run dev # Start the development server
```

- Installer le thème

```bash
npm install -D @aneoconsulting/armonik-docs-theme
```

```ts
export default defineNuxtConfig({
  extends: "@aneoconsutling/armonik-docs-theme",
});
```


Et _voilà_ !

---
layout: section
background: https://images.unsplash.com/photo-1571371293535-8f6725cfc68b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1771&q=80
---

# Écriture

---

## Markdown

<v-clicks>

- Possibilité d'utiliser la syntax étendu du [Markdown](https://markdownguide.org/)

<Alert color="blue" class="mt-4" title="Vous connaissez déjà">
Jusque là, rien de nouveau. Vous connaissez déjà le Markdown et vous savez comment l'utiliser.
</Alert>

</v-clicks>

---
seeMore:
  text: "Documentation"
  href: https://aneoconsulting.github.io/armonik-docs-theme/guide/writing/#mdc
---

## MDC

- Utilisation du [MDC](https://content.nuxtjs.org/guide/writing/mdc)

<Alert color="yellow" class="my-4" title="Nouveau">
Le MDC, Markdown Components, est une extension du Markdown, spécifique à Nuxt, qui permet d'ajouter des composants à votre documentation.
</Alert>

Exemple :

```md
::alert{type="blue"}
Je suis le contenu de l'alerte
::
```

- [Composants Disponibles](https://elements.nuxt.space/)
- Possibilité de créer ses propres composants

---
layout: two-cols
---

## Arborescence
Files based routing

::left::

```txt
content/
├── 0.index.md
├── 1.guide/
│   ├── 1.getting-started.md
│   ├── 2.configuration.md
│   ├── 3.writing.md
│   └── 4.content-directory.md
└── 2.api/
    ├── 1.components.md
    └── 2.directives.md
```

- Création des pages et routes à partir de l'arborescence des fichiers
- Ordonnancement des fichiers et des dossiers par préfixe numérique

::right::

<v-click>

| File | Path |
| --- | --- |
| content/index.md | / |
| content/about.md | /about |
| content/blog/index.md	| /blog |
| content/blog/hello.md |	/blog/hello |
| content/1.guide/2.installation |	/guide/installation |

</v-click>

---
layout: section
background: https://images.unsplash.com/photo-1591599712762-00c47efe09d8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1964&q=80
---

# Mise en ligne

---
seeMore:
  text: "GitHub Pages"
  href: https://pages.github.com/
---

## Déploiement

- Utilisation de GitHub Pages

<Alert color="blue" class="mt-4" title="Facile">

Toutes les étapes et sont expliquées dans [la documentation du thème](https://aneoconsulting.github.io/armonik-docs-theme/guide/deployment).
<br /><br />
Un **déploiement automatique** est possible grâce à GitHub Actions dont la **configuration** est également disponible dans la **documentation**.

</Alert>
