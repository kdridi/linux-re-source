# But du projet Linux [Re:Source]

**Tagline:** _"Ancient code. Modern tests."_

## Objectif principal

Reprendre le dépôt Git historique du kernel Linux et le reconstruire méthodiquement avec les pratiques de développement actuelles : tests unitaires, TDD, documentation progressive, et reproductibilité.

## Ce que nous voulons

- Repartir du code original de Linux (v0.x)
- Faire en sorte qu'il compile avec un toolchain moderne (GCC/Clang récents)
- Ajouter progressivement des tests (unitaires, d'intégration, validation)
- Documenter chaque étape comme un travail d'archéologie technique
- Préserver l'esprit d'origine du code sans le réécrire inutilement

## Ce que nous ne voulons PAS

- "Moderniser" Linux
- Faire un fork
- Réécrire le code

## Principe directeur

Chaque commit doit raconter quelque chose : comment on comprend, corrige, et valide une portion du code, avec rigueur et respect pour les développeurs d'époque.

## Ton du projet

Celui de la **transmission** et de la **compréhension**, pas de la refonte.
Chaque amélioration doit être accompagnée d'explications et de vérifications concrètes.

## Domaines d'aide attendus

- Organisation (structure, branches, conventions)
- Rédaction de tests adaptés (Catch2, gtest, etc.)
- Documentation précise (README, diagrammes, commentaires)
- Automatisation de la compilation et l'exécution (CMake, scripts build)
- Faire vivre ce projet comme un apprentissage vivant du code source

---

**Dépôt GitHub:** https://github.com/kdridi/linux-re-source
