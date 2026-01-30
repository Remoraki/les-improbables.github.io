
Bienvenue ! Ce guide vous explique comment participer à la construction collaborative de ce site.

## Pourquoi contribuer ?

Ce wiki est un **espace collaboratif** destiné à rassembler et partager des connaissances sur l'improvisation théâtrale, les formations, les exercices et les concepts pédagogiques. Votre contribution, quelle qu'elle soit, enrichit cette ressource pour tout le club des !mprobables. Les paroles s'envolent ou un truc du genre.

## Les bases à comprendre

Avant de commencer, voici les concepts clés du projet :

- **[[Markdown]]** : Le langage simple utilisé pour écrire les pages
- **[[Obsidian-Logseq]]** : Les éditeurs recommandés pour travailler sur le wiki
- **[[Quartz]]** : Le moteur qui transforme vos notes en site web
- **[[Git]]** : Le système de versioning pour collaborer

> [!TIP]
> Pas de panique ! Vous n'avez pas besoin de tout maîtriser pour commencer. Lisez ces pages pour comprendre les bases, puis lancez-vous progressivement.

## Comment contribuer ?

### Méthode 1 : Contribution directe via GitHub (recommandée)

1. **Créez un compte** sur [GitHub](https://github.com) si vous n'en avez pas
2. **Forkez** le dépôt du projet
3. **Clonez** votre fork sur votre ordinateur
4. **Modifiez ou créez** des fichiers Markdown dans le dossier `content/`
5. **Commitez** vos changements avec un message clair
6. **Poussez** vos modifications vers votre fork
7. **Créez une Pull Request** pour proposer vos changements

Plus de détails dans la page [[Git]] (si je la fais)

### Méthode 2 : Modification simple via l'interface GitHub

Pour des corrections mineures (fautes de frappe, petites améliorations) :

1. Naviguez vers le fichier sur GitHub
2. Cliquez sur l'icône "crayon" (Edit)
3. Faites vos modifications
4. Proposez les changements via "Propose changes"

## Que pouvez-vous contribuer ?

- **Exercices d'improvisation** : partagez vos exercices préférés
- **Workshops** : documentez des ateliers que vous avez animés, ou que d'autres on animé (avec leur autorisation explicite !)
- **Concepts théoriques** : expliquez des notions d'impro
- **Corrections** : améliorez l'orthographe, la clarté, la structure
- **Liens** : créez des connexions entre les pages existantes
- **Traductions** : aidez à rendre le contenu accessible à tous

Vous pouvez aussi contribuer au code, mais il y a beaucoup moins besoin, puisque le site est déjà fonctionnel.

## Bonnes pratiques

Pour ce qui est des noms de fichiers :

- Utilisez des noms descriptifs! Typiquement, évitez `Formation de Formation en Impro.md` par exemple. Ça serait stupide.
- Évitez les caractères spéciaux (sauf accents français)
- Privilégiez les espaces aux underscores

N'oubliez pas que si vous avez besoin que votre article ai un nom différent du nom de fichier, vous pouvez utiliser un [[Markdown#Frontmatter (métadonnées)|titre]] !

## Tester localement

Avant de proposer vos changements, vous pouvez testez le rendu si vous voulez :

```bash
cd source/
npx quartz build --serve
```

Ouvrez `http://localhost:8080` dans un navigateur pour voir le résultat.

## Code de conduite

- **Respectez** les contributions des autres. C'est pas cool de supprimer des pages!
- **Soyez constructif** dans vos retours!
- **Documentez** vos changements importants (au moins plus que moi, et la barre est basse)
- **Demandez** de l'aide si vous êtes bloqué! Il y aura toujours au moins un SN au club pour aider.

## Besoin d'aide ?

- Consultez les pages [[Markdown]], [[Git]], [[Quartz]] et [[Obsidian-Logseq]]
- Ouvrez une [Issue](https://github.com/les-improbables/les-improbables.github.io/issues) sur GitHub si jamais vous trouvez un bug
- Contactez les mainteneurs du projet (les gens qui participent activement)

## Ressources utiles

- [Documentation Markdown](https://www.markdownguide.org/)
- [GitHub Guides](https://guides.github.com/)
- [Documentation Quartz](https://quartz.jzhao.xyz/)
- [Documentation Obsidian](https://help.obsidian.md/)

## Note de fin

Merci de vous intéresser à contribuer. C'est cool. Avec un peu d'efforts, dans quelques années, les membres de !mprobables auront un accès facile à toutes les notions qu'on voit en impro au club, et pourront plus facilement préparer des exercices, en inventer des nouveaux, tester l'impro longue...



