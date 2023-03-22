# Groupe

Manon Bonnet
David Dehe

# Lancer le projet

npm i
npm start

# Règles de bon fonctionnement 
## Pour ajouter une feature

Créer une branche depuis main
La nommer selon la convention suivante :
- feat/... pour ajouter une feature
- fix/... pour corriger un bug
- docs/... pour mettre à jour la doc
- tests/... pour ajouter des tests

Faire une PR de cette branche sur dev une fois que les tests sont passés. (Actions)
Une fois qu'une personne ayant les droits pour valider la PR, le merge sera fait.

Une fois merge sur main et les tests passés, Jenkins fera un build (main équivalent à la pré prod).
Si le build passe, on peut merge main sur la branche protégée PROD qui donnera lieu à un nouveau build Jenkins.

## La validation d'une feature

Personne ne peut push sur main et prod
Seul l'integration manager peut merge une branche de feature sur main, une fois qu'il l'a validée


## Vérifier les étapes

Pour que Jenkins se lance, les actions github doivent toutes passer.
Quand Jenkins a fait un build, il y a un retour dans github dans les webhooks.

# La configuration Jenkins

Dans Jenkins, pour les builds, il y a des pipelines qui sont lancées quand un merge est fait dans main et dans prod.
Cela revient à builder le projet en pré-prod et en prod.

Ces pipelines ne sont lancées que si les Actions github passent. 

## Les étapes de construction du tic tac toe

Pour chaque feature, une branche est créée avec la nommenclature décidée précédemment. Une fois prête elle peut être push.

Si les Actions github passent une PR peut être ouverte, les autres contributeurs du github peuvent faire la review de cette PR, la valider ou non.

Si la PR est validée, l'integration manager peut merge la branche sur main. 

Une fois merge, un nouveau build est lancé par Jenkins et d'autres features peuvent être apportées au projet !
