
## Qu'est-ce que Quartz ?

**Quartz** est un générateur de site statique (SSG - Static Site Generator) conçu spécifiquement pour transformer des notes en [[Markdown]] en un site web entièrement fonctionnel. Il a été créé par [Jacky Zhao](https://jzhao.xyz/) pour publier des jardins numériques (digital gardens). Et surtout, c'est **open-source** (oui bah je suis biaisé mais c'est pratique)
## Configuration

### Fichier `quartz.config.ts`

Ce fichier contrôle le comportement global :

```typescript
const config: QuartzConfig = {
  configuration: {
    pageTitle: "Wiki Improbables",
    enableSPA: true,
    enablePopovers: true,
    baseUrl: "les-improbables.github.io",
    // ...
  },
  plugins: {
    transformers: [...],
    filters: [...],
    emitters: [...],
  },
}
```

### Fichier `quartz.layout.ts`

Ce fichier définit la disposition des composants :

```typescript
export const defaultContentPageLayout: PageLayout = {
  beforeBody: [
    Component.Breadcrumbs(),
    Component.ArticleTitle(),
  ],
  left: [
    Component.PageTitle(),
    Component.MobileOnly(Component.Spacer()),
    Component.Search(),
    Component.Darkmode(),
    Component.DesktopOnly(Component.Explorer()),
  ],
  right: [
    Component.Graph(),
    Component.DesktopOnly(Component.TableOfContents()),
    Component.Backlinks(),
  ],
}
```

## Utiliser Quartz localement

### Installation

```bash
cd source/
npm install  # ou pnpm install
```

### Build du site

```bash
npx quartz build
```

Génère le site dans `public/`

### Serveur de développement

```bash
npx quartz build --serve
```

Ouvre un serveur local sur `http://localhost:8080` avec rechargement automatique.

### Options utiles

```bash
# Build + serve avec hot reload
npx quartz build --serve

# Build rapide (sans optimisations)
npx quartz build --fastRebuild

# Nettoyer le cache
npx quartz build --clean
```

## Déploiement

Ce wiki est automatiquement déployé sur **GitHub Pages** via GitHub Actions :

1. Push vers la branche `main`
2. GitHub Actions lance le build Quartz
3. Le site généré est publié sur `les-improbables.github.io`

> [!TIP]
> Vous n'avez pas besoin de builder localement pour contribuer ! Le build se fait automatiquement sur GitHub. N'est-ce pas magnifique. J'en ai les larmes aux yeux.

## Personnalisation

### Thème

Les couleurs sont définies dans `quartz.config.ts` :

```typescript
theme: {
  colors: {
    lightMode: {
      light: "#faf8f8",
      dark: "#141021",
      // ...
    },
    darkMode: {
      light: "#161618",
      dark: "#eeeeee",
      // ...
    },
  },
}
```

### Composants

Créez de nouveaux composants dans `quartz/components/` :

```typescript
// quartz/components/MonComposant.tsx
export default (() => {
  function MonComposant({ fileData, cfg }: QuartzComponentProps) {
    return <div>Mon contenu</div>
  }
  return MonComposant
}) satisfies QuartzComponentConstructor
```
## MoutonQuartz (ce projet)

Ce wiki utilise une version **forkée et personnalisée** de Quartz appelée **MoutonQuartz** :

- Thème personnalisé adapté au projet
- Fonctionnalités spécifiques ajoutées (par exemple la barre de navigation sur mobile (et oui))

Le code source du fork est dans le dossier `quartz/`.

> [!NOTE]
> Ça veut dire que si on a besoin de fonctionnalités en plus, on peut les implémenter facilement.

## Ressources

- [Documentation officielle Quartz](https://quartz.jzhao.xyz/)
- [GitHub Quartz](https://github.com/jackyzha0/quartz)
- [Discord Quartz](https://discord.gg/cRFFHYye7t)

## Voir aussi

- [[Markdown]] - Format source des pages
- [[Git]] - Versionnage et collaboration
- [[Obsidian-Logseq]] - Édition du contenu
- [[Comment contribuer]] - Guide complet de contribution
