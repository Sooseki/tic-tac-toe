# Getting Started with Tic tac toe app

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Pour lancer le projet

npm i
npm start

## Pour ajouter une feature

Créer une branche depuis main
La nommer feat/xxx - fix/xxx etc... pour indiquer le type de feature.

Faire une PR de cette branche sur dev une fois que les tests sont passés. (Actions)
Une fois qu'une personne ayant les droits pour valider la MR, le merge sera fait.

Une fois merge sur main, Jenkins fera un build (main équivalent à la pré prod).
Si le build passe, on peut merge main sur la branche protégée PROD qui donnera lieu à un nouveau build Jenkins.

## Les branches protégées

Personne ne peut push sur main et prod
Seul le lead dev peut merge une branche de feature sur main
Seul Jenkins peut valider le merge de main sur la branche prod