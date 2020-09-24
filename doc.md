## TASK 2

### 2.1 interface language

L'interet de regrouper les Strings de l'application en dehors du layout dans un fichier xml est de pouvoir faciliter les traductions, en effet pas besoins de toucher le code de l'application ou de connaitre le kotlin/java, il suffit au traducteur d'ajouter un fichier xml de la nouvelle langue. C'est une très bonne pratique pour tous ce qui est correction de fautes aussi.

Pour avoir une app multi-langues, il suffit d'organiser les fichiers strings.xml ainsi:

```bash
res
├── drawable
│   ├── ic_launcher_background.xml
│   └── ic_launcher_foreground.xml
├── layout
│   └── activity_main.xml
.
.
.
├── values
│   ├── colors.xml
│   ├── dimen.xml
│   ├── ic_launcher_background.xml
│   ├── strings.xml
│   └── styles.xml
├── values-de
│   └── strings.xml
└── values-fr
    └── strings.xml
```

on voit qu'on a des values pour fr et de, si par exemple on a son android en fr, values-fr est chargé, si c'est une autre langue que fr ou de, c'est values qui est chargé (par defaut), s'il manque des fichier xml ou qu'ils sont incomplet dans values-fr ou values-de, les values par défaut sont chargée pour ce qui manque.
