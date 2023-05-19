# Gitflow Workflow sur GitHub

Le Gitflow Workflow est un modèle de gestion de branches Git qui est particulièrement adapté pour les projets avec un cycle de développement long et plusieurs versions en production. Ce guide explique comment mettre en place le workflow Gitflow sur GitHub.

## Branches Gitflow

Le Gitflow Workflow utilise deux branches principales : `master` et `develop`. La branche `master` contient le code qui est en production, tandis que la branche `develop` contient le code qui est en cours de développement. En plus de ces deux branches principales, le Gitflow Workflow utilise des branches secondaires pour les fonctionnalités et les corrections de bugs.

## Configuration

Pour configurer le Gitflow Workflow sur GitHub, suivez les étapes suivantes :

1. Créez un dépôt sur GitHub pour votre projet.
2. Clonez le dépôt sur votre ordinateur.
3. Installer git flow
4. Configurez Git pour utiliser le workflow Gitflow :

   ```
   git flow init -d
   ```

Cette commande initialise le workflow Gitflow avec les paramètres par défaut.

5. Configurez les branches sur GitHub en poussant les branches locales sur GitHub :

```
git push -u origin master
git push -u origin develop
```

Ces commandes poussent les branches master et develop locales sur GitHub.

## Workflow

Une fois que vous avez configuré le Gitflow Workflow sur GitHub, vous pouvez commencer à travailler sur votre projet. Voici les étapes pour le workflow Gitflow :

1. Créez une branche pour une fonctionnalité :

```
git flow feature start my-feature
```

Cette commande crée une branche pour la fonctionnalité `my-feature`.

2. Travaillez sur la branche de la fonctionnalité.
3. Publiez la branche de la fonctionnalité sur GitHub :
```
git flow feature publish my-feature
```
Cette commande pousse la branche de la fonctionnalité sur GitHub.

4. Créez une demande de fusion (pull request) pour la branche de la fonctionnalité sur GitHub.
5. Faites une revue de code et fusionnez la branche de la fonctionnalité dans la branche `develop`.
```
 git flow feature finish my-feature
```
Cette commande fusionne la branche de la fonctionnalité dans la branche `develop`.
6. Publiez la branche `develop` sur GitHub :
```
git flow publish develop
```
Cette commande pousse la branche `develop` sur GitHub.

7. Créez une nouvelle branche pour la prochaine fonctionnalité ou correction de bug :
```
git flow feature start next-feature
```
Cette commande crée une nouvelle branche pour la prochaine fonctionnalité ou correction de bug.
8. Répétez les étapes 2 à 7 pour chaque fonctionnalité ou correction de bug.

## Conclusion

Le Gitflow Workflow est un modèle de gestion de branches Git qui est adapté pour les projets avec un cycle de développement long et plusieurs versions en production. En suivant ce guide, vous pouvez mettre en place le Gitflow Workflow sur GitHub pour votre projet.









































