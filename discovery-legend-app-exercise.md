# Découverte de Legend App

A la fin de cet exercice vous connaîtrez les bases de Legend App, vous permettant ainsi de créer des `observables`.

## Partie 1 : Créer mon template

### La TODO

1. Créer une application react avec vite et typescript
2. Installer les dépendances `@legendapp/state`
3. Créer un composant comportant :
   1. un formulaire avec un champ `input` et un `label` pour des champs :
      1. firstname
      2. lastname
      3. Une concaténation des deux précédentes valeurs

### Résultat attendu
Lorsque vous irez sur la home page de votre application, vous devriez avoir :

## Partie 2 : Ajouter son premier `observable`

### La TODO

1. Utiliser le hook `useObservable` pour créer un observable `person`, composé des champs `firstname` et `lastname`, avec comme valeur par défaut `John` et `Doe`
2. Affecter les valeurs des champs `firstname` et `lastname` aux champs correspondants du formulaire
3. Brancher le champ `fullname` à l'observable `person`
4. Ajouter le gestionnaire d'événement `onChange` sur les champs `firstname` et `lastname` pour mettre à jour l'observable `person`

### Résultat attendu

Une fois cette partie effectuée, vous devriez avoir un formulaire avec des valeurs par défaut mais lorsque vous éditez un champs, rien ne se passe.

## Partie 3 : Faire que son composant soit `aware`

### La TODO

1. Importer la dépendance `observer`
2. Entourer le composant avec le `observer`

### Résultat attendu 

Maintenant tout est synchronisé avec l'observable `person`.

## Partie 4 : Partager un observable

### La TODO

1. Créer un composant `Firstname` avec un champ `input` et un `label` pour le champ `firstname`
2. Créer un composant `Lastname` avec un champ `input` et un `label` pour le champ `lastname`
3. Créer un composant `Fullname` avec un champ de concaténation pour les champs `firstname` et `lastname`
4. Adapter l'appel des nouveaux composants au `Composant`

### Résultat attendu

Vous devriez avoir le même résultat qu'à la fin de la partie 2 mais de nouveau, la mise à jour des champs ne fonctionne pas. Pour remédier au problème, chacun des composants doit être `aware`. Un exemple avec le composant `Firstname`

## Partie 5 : Faire que son composant soit `aware`

### La TODO

1. Importer la dépendance `observer`
2. Entourer le composant avec le `observer`

### Résultat attendu 

Maintenant tout est synchronisé avec l'observable `person`.

## Partie 6 : Partager via le `context`

Le but de cette partie est de pourvoir localiser l'impact des changements d'état. Si vous souhaitez créer deux formulaires dans votre composant, actuellement, ils vont partager le même état, ce qui n'est pas souhaitable. Pour cela, nous allons utiliser le `context` de React.

### La TODO

1. Créer un context `PersonContext` avec comme valeur par défaut l'observable `person`
2. Créer un composant `Form` qui contiendra les composants `Firstname`, `Lastname` et `Fullname`.

### Résultat attendu

Vous devriez avoir le même résultat qu'à la fin de la partie 5 à ceci près que vous pouvez créer plusieurs formulaires indépendants.

# Bon courage !