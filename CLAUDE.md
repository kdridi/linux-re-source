# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Vue d'ensemble du projet

**Linux [Re:Source]** - _"Ancient code. Modern tests."_

Projet d'archéologie technique : reconstruction méthodique du kernel Linux historique (v0.x) avec les pratiques modernes de développement (tests, TDD, documentation, reproductibilité).

**Ce n'est PAS un fork ni une modernisation de Linux**, mais une démarche pédagogique de compréhension et validation du code original.

## Répertoire Claude

Toutes les interactions et demandes sont documentées dans le répertoire `claude/` :
- `claude/00-but-du-projet.md` : objectifs et principes du projet
- `claude/01-strategie-commits.md` : stratégie de progression commit par commit
- `claude/XX-*.md` : autres documents d'interactions et décisions

**Important :** Consulter systématiquement les fichiers du répertoire `claude/` pour comprendre le contexte et les décisions prises.

## Stratégie de progression

**Un commit Linux = un cycle complet dans notre dépôt :**

1. Avancer le submodule `linux/` d'un commit
2. Analyser les changements introduits
3. Adapter pour compilation moderne si nécessaire
4. Écrire des tests de validation
5. Documenter (technique + historique + apprentissages)
6. Commiter notre travail avec référence au commit Linux

Voir `claude/01-strategie-commits.md` pour les détails complets.

## Principes de travail

1. **Respect du code original** : ne pas réécrire, mais comprendre et valider
2. **Documentation méthodique** : chaque étape doit être expliquée
3. **Tests progressifs** : validation concrète du comportement
4. **Ton pédagogique** : transmission et compréhension avant tout

## Langue

**Toute la documentation doit être en français.**

## Convention de commits

Format : `[vX.XX] type: description`

Types :
- `archaeo` : analyse et documentation du code original
- `port` : adaptation pour compilation moderne
- `test` : ajout de tests
- `doc` : documentation
- `build` : configuration de build

## Branches proposées

- `main` : branche stable documentée
- `linux-vX.XX` : travail sur une version spécifique
- `feature/*` : fonctionnalités spécifiques

## Structure du projet

```
linux-re-source/
├── linux/                    # Submodule Git du kernel Linux
├── claude/                   # Documentation des interactions et décisions
├── docs/
│   └── commits/              # Analyse détaillée de chaque commit Linux
│       └── <hash>.md
├── tests/
│   └── <hash>/               # Tests unitaires/intégration par commit
├── ports/                    # Adaptations pour compilation moderne
│   └── <hash>/
├── scripts/                  # Automatisation du workflow
└── CLAUDE.md                 # Ce fichier
```

## Format des commits

```
[linux@<short-hash>] type: titre du commit original

Commit Linux original : <hash complet>
Auteur : <auteur> <date>
Message original :
  > <message original>

Notre travail :
- Analyse : docs/commits/<hash>.md
- Tests : tests/<hash>/
- Adaptations : ports/<hash>/

Ce que ce commit apporte :
<explication pédagogique>

Ce que nous avons testé :
<validations effectuées>

Apprentissages :
<insights techniques et historiques>
```

---

**Dépôt GitHub :** https://github.com/kdridi/linux-re-source
