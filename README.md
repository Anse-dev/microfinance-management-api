
# Microfinance Management API

Ce projet est une API de gestion de microfinance, construite avec NestJS en respectant les principes de la Clean Architecture. Elle permet la gestion des clients, comptes, transactions financières, produits financiers (prêts, épargnes, etc.), et fournit des rapports et analyses financières.

## Structure du Projet

```
src/
├── application/
│   ├── ports/
│   │   ├── in/
│   │   │   ├── create-client-input.port.ts
│   │   │   ├── create-account-input.port.ts
│   │   │   ├── create-transaction-input.port.ts
│   │   │   ├── create-product-input.port.ts
│   │   │   └── generate-report-input.port.ts
│   │   └── out/
│   │       ├── create-client-output.port.ts
│   │       ├── create-account-output.port.ts
│   │       ├── create-transaction-output.port.ts
│   │       ├── create-product-output.port.ts
│   │       └── generate-report-output.port.ts
│   ├── use-cases/
│   │   ├── create-client.interactor.ts
│   │   ├── create-account.interactor.ts
│   │   ├── create-transaction.interactor.ts
│   │   ├── create-product.interactor.ts
│   │   └── generate-report.interactor.ts
│   ├── services/
│   │   ├── client.service.ts
│   │   ├── account.service.ts
│   │   ├── transaction.service.ts
│   │   └── product.service.ts
│   └── presenters/
│       ├── client.presenter.ts
│       ├── account.presenter.ts
│       ├── transaction.presenter.ts
│       ├── product.presenter.ts
│       └── report.presenter.ts
├── domain/
│   ├── entities/
│   │   ├── client.entity.ts
│   │   ├── account.entity.ts
│   │   ├── transaction.entity.ts
│   │   └── product.entity.ts
│   └── repositories/
│       ├── client.repository.ts
│       ├── account.repository.ts
│       ├── transaction.repository.ts
│       └── product.repository.ts
├── infrastructure/
│   ├── controllers/
│   │   ├── client.controller.ts
│   │   ├── account.controller.ts
│   │   ├── transaction.controller.ts
│   │   └── product.controller.ts
│   ├── repositories/
│   │   ├── client.repository.impl.ts
│   │   ├── account.repository.impl.ts
│   │   ├── transaction.repository.impl.ts
│   │   └── product.repository.impl.ts
│   └── presenters/
│       ├── client.presenter.impl.ts
│       ├── account.presenter.impl.ts
│       ├── transaction.presenter.impl.ts
│       ├── product.presenter.impl.ts
│       └── report.presenter.impl.ts
├── main.ts
├── app.module.ts
└── swagger.ts
```

## Installation

1. Clonez le dépôt :
   ```sh
   git clone 
   cd microfinance-management-api
   ```

2. Installez les dépendances :
   ```sh
   npm install
   ```

3. Configurez la base de données et les variables d'environnement dans un fichier `.env`.

## Démarrage

Pour démarrer le serveur de développement :
```sh
npm run start:dev
```

## Documentation de l'API

Cette API utilise Swagger pour la documentation. Après avoir démarré l'application, accédez à la documentation Swagger via :
```
http://localhost:3000/api
```

## Tests

### Tests unitaires
Pour exécuter les tests unitaires :
```sh
npm run test
```

### Tests fonctionnels (end-to-end)
Pour exécuter les tests fonctionnels :
```sh
npm run test:e2e
```

## Fonctionnalités

- **Gestion des clients** : Création, mise à jour, suppression et consultation des clients.
- **Gestion des comptes** : Création, mise à jour, suppression et consultation des comptes.
- **Enregistrement des transactions financières** : Dépôts, retraits et transferts.
- **Gestion des produits financiers** : Prêts, épargnes, etc.
- **Rapports et analyses financières** : Génération de divers rapports financiers.

## Structure de la Clean Architecture

- **Application** : Contient les cas d'utilisation, services et ports (interfaces).
- **Domaine** : Contient les entités et les interfaces des dépôts.
- **Infrastructure** : Contient les implémentations des dépôts, contrôleurs et présentateurs.

## Contribuer

Les contributions sont les bienvenues. Veuillez suivre les étapes suivantes pour contribuer :

1. Fork le projet
2. Créez votre branche de fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. Commitez vos changements (`git commit -m 'Add some AmazingFeature'`)
4. Poussez votre branche (`git push origin feature/AmazingFeature`)
5. Ouvrez une Pull Request

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
