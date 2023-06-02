# Giter RESET
La commande git reset est utilisée pour déplacer la branche courante et/ou l'index vers un commit spécifié, ce qui permet d'annuler ou de réorganiser l'historique des commits. Elle peut être utilisée de différentes manières en fonction des options fournies. Voici quelques utilisations courantes de git reset :

## Annuler les modifications locales non confirmées :
```
bashgit reset --hard HEAD
```
Cette commande annule toutes les modifications non confirmées dans le répertoire de travail et rétablit l'index et la branche courante à l'état du dernier commit.

## Supprimer un commit spécifique et annuler ses modifications :
```
bashgit reset --hard <commit>
```
Remplace la branche courante et l'index par le commit spécifié, annulant ainsi les commits ultérieurs et supprimant les modifications correspondantes de l'historique. Cette commande doit être utilisée avec prudence, car les commits supprimés peuvent être difficiles à récupérer.

## Annuler un commit tout en conservant les modifications dans l'index :
```
bashgit reset --soft <commit>
```
Déplace la branche courante vers le commit spécifié tout en conservant les modifications du commit dans l'index. Les modifications apparaîtront comme étant "à valider" (staged), vous permettant de réexécuter le commit avec des modifications supplémentaires ou de les annuler complètement.

## Déplacer la branche courante sans modifier l'index ou le répertoire de travail :
```
bashgit reset <commit>
```
Déplace simplement la branche courante vers le commit spécifié, sans modifier l'index ni le répertoire de travail. Les modifications restent dans l'index en tant que modifications non confirmées.

## Annuler les commits et fusionner les modifications dans un nouveau commit :
```
bashgit reset --mixed <commit>
```
Déplace la branche courante vers le commit spécifié, annulant les commits ultérieurs. Les modifications des commits annulés sont ajoutées à l'index en tant que modifications non confirmées, vous permettant de créer un nouveau commit consolidant les modifications.

Il est important de noter que l'utilisation de git reset peut modifier l'historique des commits, il est donc recommandé de l'utiliser avec prudence et de comprendre ses implications. N'hésitez pas à consulter la documentation officielle de Git ou à me poser des questions supplémentaires si nécessaire !