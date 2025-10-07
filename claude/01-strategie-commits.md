# Stratégie de progression : Un commit pour un commit

## Principe fondamental

**Chaque commit original de Linux = un cycle complet d'analyse, modernisation, test et documentation dans notre dépôt.**

Nous voulons comprendre, moderniser, documenter ET présenter **CHAQUE** commit original de Linux, de manière exhaustive.

## Workflow pour chaque commit Linux

1. **Avancer le submodule** d'un commit
2. **Analyser** ce que le commit change (code, architecture, intention)
3. **Adapter/moderniser** si nécessaire (build moderne, compatibilité toolchain)
4. **Écrire des tests** pour valider le comportement introduit/modifié
5. **Documenter** (explication technique + contexte historique + apprentissages)
6. **Commiter notre travail** avec référence explicite au commit Linux

## Structure du dépôt

```
linux-re-source/
├── linux/                           # submodule git du kernel Linux
├── claude/                          # Documentation des interactions
│   ├── 00-but-du-projet.md
│   └── 01-strategie-commits.md
├── docs/
│   └── commits/
│       └── <hash>.md                # Analyse détaillée de chaque commit
├── tests/
│   └── <hash>/                      # Tests unitaires/intégration par commit
├── ports/                           # Adaptations modernes si nécessaire
│   └── <hash>/                      # Code adapté pour compilation moderne
└── scripts/
    └── next-commit.sh               # Automatisation du workflow
```

## Format de nos commits

```
[linux@<short-hash>] type: titre du commit Linux original

Commit Linux original : <hash complet>
Auteur : <auteur> <date>
Message original :
  > <message du commit Linux tel quel>

Notre travail :
- Analyse : docs/commits/<hash>.md
- Tests : tests/<hash>/
- Adaptations : ports/<hash>/ (si nécessaire)

Ce que ce commit apporte :
<explication pédagogique détaillée>

Ce que nous avons testé :
<liste des tests ajoutés et validations effectuées>

Apprentissages :
<ce que ce commit nous apprend sur Linux, le C, l'architecture, etc.>
```

## Types de commits

- `archaeo` : analyse et documentation du commit original
- `port` : adaptation pour compilation moderne
- `test` : ajout de tests de validation
- `doc` : documentation complémentaire
- `build` : configuration de build/outils

## Points à définir

1. **Point de départ** : tout premier commit Linux ou version 0.01 ?
2. **Rythme de progression** : nombre de commits à traiter par session
3. **Critères de qualité** : niveau de couverture de tests attendu
4. **Outils de tests** : framework(s) à utiliser (Catch2, gtest, custom...)
5. **Build system** : CMake, Make, ou autre ?

## Philosophie

Cette démarche est **exhaustive et chronologique** : nous suivons l'histoire de Linux commit par commit, sans en sauter, pour comprendre comment le système s'est construit progressivement.

C'est un travail d'**archéologie technique minutieux** où chaque pierre (commit) est examinée, nettoyée, testée et expliquée.
