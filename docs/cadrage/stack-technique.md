# Stack Technique & Outils — Blog des Lauréats

**Projet :** Blog des Lauréats (plateforme Web et application mobile de consultation d'articles)  
**Méthodologie :** Agile/Scrum et TDD (Test-Driven Development)

## 1. Exigences Techniques

Le projet doit répondre aux exigences suivantes :

- Garantir un chargement rapide des listes d'articles et des profils de lauréats.
- Assurer une séparation claire entre l'interface utilisateur, la logique métier et l'accès aux données.
- Protéger l'application contre les injections SQL, les attaques XSS et CSRF.
- Garantir une authentification sécurisée des auteurs et des administrateurs.
- Proposer une interface responsive adaptée aux ordinateurs, tablettes et smartphones.
- Limiter l'application Android native à la consultation et à la lecture des articles.

## 2. Backend

### Laravel

Laravel, basé sur PHP, est retenu pour répondre aux besoins du projet grâce aux avantages suivants :

- Son architecture MVC permet de séparer la présentation, la logique applicative et l'accès aux données.
- Eloquent ORM simplifie la gestion des lauréats, des articles, des catégories et des utilisateurs.
- Blade permet de créer des interfaces Web avec des composants et des layouts réutilisables.
- Les Middleware permettent de centraliser la gestion des autorisations des administrateurs et des auteurs.
- Les mécanismes intégrés de validation et de protection contre les CSRF, XSS et injections SQL contribuent à la sécurité de l'application.
- Laravel peut être utilisé dans le cadre du développement Web et de la solution mobile NativePHP.

### MySQL

MySQL est retenu pour la gestion des données structurées du projet grâce aux caractéristiques suivantes :

- Les clés étrangères garantissent l'intégrité des relations entre les utilisateurs, les articles, les catégories et les lauréats.
- Les transactions ACID permettent de sécuriser les opérations de modification des données.
- Son intégration avec Laravel et Eloquent ORM est mature et facile à mettre en place.
- Il permet de travailler aussi bien dans un environnement de développement local sous Windows que dans un environnement de production.

## 3. Frontend

### Tailwind CSS

Tailwind CSS est retenu pour les raisons suivantes :

- Il permet de développer rapidement une interface cohérente et responsive.
- Ses classes utilitaires réduisent le besoin de créer des feuilles CSS personnalisées.
- Ses breakpoints facilitent l'adaptation des interfaces aux ordinateurs, tablettes et smartphones.
- Vite optimise les ressources CSS lors de la préparation du build de production.

### Preline UI

Preline UI est retenu pour les avantages suivants :

- Il propose des composants prêts à l'emploi compatibles avec Tailwind CSS, tels que les cartes, menus, dialogues et formulaires.
- Il accélère le développement des interfaces.
- Il s'intègre à Tailwind CSS et aux vues Blade sans nécessiter l'adoption d'un framework frontend complexe.

### Alpine.js

Alpine.js est retenu pour gérer les interactions légères de l'application :

- Il permet de gérer les menus, filtres, modales et notifications.
- Il évite d'introduire un framework frontend complet pour les interactions nécessaires.
- Il réduit la complexité du JavaScript.
- Il s'intègre directement aux pages générées avec Blade.

## 4. Développement Mobile

### NativePHP

NativePHP est retenu pour développer la version Android du projet, dont les fonctionnalités sont limitées à la consultation des articles :

- Il permet de créer une application mobile native à partir de l'écosystème PHP et Laravel.
- Il permet de réutiliser une partie importante du code et des composants existants de Laravel.
- Il évite, dans le cadre de cette approche, de maintenir deux projets applicatifs entièrement distincts.
- Il permet de concentrer le développement mobile sur les fonctionnalités de navigation et de lecture des articles.

| Critère | NativePHP | API + Flutter/React Native |
|---|---|---|
| Codebase | Réutilisation d'une grande partie du code existant | Deux environnements applicatifs distincts |
| Développement | Approche simplifiée pour le périmètre du projet | Développement supplémentaire |
| Maintenance | Centralisation d'une partie importante de la logique | Maintenance de deux applications |
| Adéquation | Adapté à une application de consultation avec un périmètre limité | Approche plus complète, mais potentiellement plus complexe |

## 5. Qualité et Outils d'Assistance IA

### Tests Automatisés

Les tests automatisés sont retenus afin de respecter la méthodologie TDD et de prévenir les régressions :

- PHPUnit ou Pest permettent de mettre en œuvre le cycle Red-Green-Refactor dans l'écosystème Laravel.
- Les tests unitaires et fonctionnels vérifient la création, l'affichage, le filtrage des articles et les règles d'accès.
- Les tests sont exécutés avant les phases d'intégration et de déploiement.
- Ils permettent de vérifier le fonctionnement des fonctionnalités après chaque modification.

### Assistance par l'Intelligence Artificielle

#### GitHub Copilot

GitHub Copilot est retenu comme outil d'assistance au développement :

- Il s'intègre à l'environnement de développement.
- Il facilite la rédaction de code PHP et Laravel.
- Il peut assister dans la création des migrations, factories, validations et tests.
- Il réduit la rédaction répétitive de code.
- Les propositions générées doivent être vérifiées, testées et validées par le développeur.

#### Antigravity

Antigravity est retenu comme outil d'assistance pour les tâches de développement impliquant plusieurs fichiers :

- Il facilite la réalisation de tâches impliquant les modèles, contrôleurs, vues, routes et tests.
- Il aide à produire et structurer la documentation technique.
- Il permet d'assister dans les tâches répétitives liées au terminal.
- Il facilite la vérification de la cohérence entre les spécifications et les différentes parties du projet.

