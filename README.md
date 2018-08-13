# react-redux test

Se base sur l'exemple Todomvc de Redux.

1. Prendre connaissance de l'application

Faire un tour global et décrire les objets et le découpage

2. Créer les actions et reducer

Objectif : Brancher les composants graphiques aux reducers

L'objectif est de:
  - Ajouter une tâche
  - Lister des tâches
  - Supprimer une tâche
  - Marquer une tâche comme finie
  - Marquer une tâche comme à faire

NB :
  - Un reducer `todos` avec la liste des todos, l'ajout, modification, la suppression, changement de status unitaire ou tous.
  - Un reducer `visibilityFilter` contenant le filtre actif. Tout afficher par défaut.
  - L'objet `Todo` a la forme suivante

```json
{
  id: int,
  completed: bool,
  text: string
} 
```

Tip : Obtenir un nouvel id de todo
	state.reduce((maxId, todo) => Math.max(todo.id, maxId), -1) + 1

3. Câbler à une API

Objectif :  Initialiser la liste des tâches via l'appel à un endpoint sur l'API

Récupérer le projet github : https://github.com/yyekhlef/todo-aspnetcore

Lancer avec Docker l'API

4. HTML/CSS

  Afficher des blocs en mode card/carte :
    - 3 ou 4 cartes par ligne pour un écran desktop large
    - 2 cartes par ligne pour un écran moyen
    - 1 carte pour le mobil

5. En option : Filtrer les tâches

  - Ajouter une zone de recherche et filtrer les tâches
  - Ajouter un throttle pour ne filtrer qu'après le troisième caractère

6. En option : Ajouter un endpoint retournant la version de l'api