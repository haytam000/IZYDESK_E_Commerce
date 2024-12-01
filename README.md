# IZYDESK_E_Commerce
Voici un modèle de fichier README pour une application Symfony dédiée à un "PC Store" (magasin de PC). Ce fichier explique les étapes nécessaires pour installer, configurer et utiliser l'application.

```markdown
# PC Store - Application Symfony

Bienvenue dans le projet PC Store ! Cette application Symfony permet de gérer un magasin de PC en ligne. Elle inclut des fonctionnalités telles que la gestion des produits, des catégories, des utilisateurs, et des commandes.

## Prérequis

Avant de commencer, assurez-vous que vous disposez des outils suivants installés sur votre machine :

- **PHP 8.1 ou supérieur** : Vous pouvez vérifier la version de PHP avec la commande `php -v`.
- **Composer** : Utilisé pour gérer les dépendances du projet. Vous pouvez l'installer en suivant les instructions sur le site officiel : https://getcomposer.org/.
- **MySQL** ou tout autre serveur de base de données compatible avec Doctrine.
- **Node.js** et **npm** : Pour la gestion des assets frontend.

## Installation

### 1. Clonez le projet

Commencez par cloner le repository sur votre machine locale :

```bash
git clone https://votre-repository-url/pc-store.git
cd pc-store
```

### 2. Installez les dépendances PHP avec Composer

Dans le répertoire du projet, exécutez la commande suivante pour installer les dépendances PHP :

```bash
composer install
```

### 3. Configurez votre base de données

Modifiez le fichier `.env` ou `.env.local` pour définir les paramètres de votre base de données. Exemple :

```env
DATABASE_URL="mysql://root:password@127.0.0.1:3306/pc_store"
```

### 4. Créez la base de données

Ensuite, créez la base de données en exécutant la commande suivante :

```bash
php bin/console doctrine:database:create
```

### 5. Exécutez les migrations

Appliquez les migrations pour créer les tables de la base de données :

```bash
php bin/console doctrine:migrations:migrate
```

### 6. Installez les dépendances frontend

Si le projet utilise des assets frontend, vous devrez installer les dépendances Node.js et compiler les assets :

```bash
npm install
npm run dev
```

### 7. Démarrez le serveur Symfony

Vous pouvez démarrer le serveur local Symfony avec la commande suivante :

```bash
symfony serve
```

L'application sera accessible à l'adresse : `http://localhost:8000`

## Fonctionnalités

L'application PC Store comprend plusieurs fonctionnalités essentielles pour gérer un magasin de PC :

- **Gestion des produits** : Ajouter, modifier et supprimer des produits dans le magasin (PC, accessoires, etc.).
- **Catégories de produits** : Organiser les produits en différentes catégories.
- **Gestion des utilisateurs** : Permettre aux utilisateurs de s'inscrire, se connecter, et passer des commandes.
- **Panier d'achat** : Ajouter des produits au panier et procéder à l'achat.
- **Commandes** : Suivi des commandes passées par les utilisateurs.

## Structure du projet

Le projet est structuré comme suit :

```
/config           - Fichiers de configuration du projet
/src              - Code source de l'application
  /Controller     - Contrôleurs pour gérer les requêtes HTTP
  /Entity         - Entités Doctrine pour la base de données
  /Repository     - Repositories pour interagir avec les entités
  /Service        - Services pour la logique métier
/public           - Fichiers accessibles publiquement (images, CSS, JS)
/templates        - Templates Twig pour l'interface utilisateur
/tests            - Tests unitaires et fonctionnels
```

## Tests

Les tests sont exécutés à l'aide de PHPUnit. Pour lancer les tests, utilisez la commande suivante :

```bash
php bin/phpunit
```

## Contributions

Les contributions sont les bienvenues ! Si vous avez des suggestions ou des améliorations à proposer, veuillez créer une pull request. Assurez-vous de suivre les bonnes pratiques de développement et d'écrire des tests pour vos modifications.

## Auteurs

- **Nom de l'auteur 1** - *Développeur principal*
- **Nom de l'auteur 2** - *Développeur backend*

## License

Ce projet est sous la licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

```

### Explication des sections :
1. **Prérequis** : Liste les outils nécessaires pour faire fonctionner le projet.
2. **Installation** : Décrit les étapes pour configurer l'environnement de développement.
3. **Fonctionnalités** : Donne un aperçu des fonctionnalités principales de l'application.
4. **Structure du projet** : Explique l'organisation des fichiers et dossiers du projet.
5. **Tests** : Décrit comment exécuter les tests unitaires.
6. **Contributions** : Invite à participer au projet.
7. **Auteurs** : Mentionne les personnes ayant travaillé sur le projet.
8. **Licence** : Spécifie sous quelle licence le projet est distribué.

N'hésitez pas à ajuster ce fichier README selon les spécificités de votre projet !
