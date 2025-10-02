
## Test technique – Développeur Node.js (30 minutes)
### EX 1
Sous-tableaux avec somme cible
On te donne :

```
const nums = [1, 2, 3, 4, 2];
const target = 5;
```
Trouver tous les sous-tableaux consécutifs dont la somme des éléments est égale à target.
"Sous-tableau consécutif" signifie que tu prends des éléments à la suite, sans sauter de valeur.

Par exemple, dans [1,2,3,4,2] :
[2,3] → 2+3 = 5
[3,2] → 3+2 = 5   
[5] → si tu avais un 5 direct dans le tableau, ce serait valide aussi.

Donc pour notre tableau [1,2,3,4,2] :
[2,3] = 5
[3,2] = 5
[5] n’existe pas ici, donc pas inclus.

### EX 2
Test technique – Développeur Node.js (30 minutes)

Implémentez une fonction fetchUrls(urls) qui :
* Reçoit en paramètre un tableau d’URLs.
* Effectue une requête HTTP sur chacune de ces URLs.
* Retourne un tableau contenant les réponses JSON dans le même ordre que les URLs fournies.
* (Bonus) Limitez le nombre de requêtes exécutées en parallèle à 3 maximum (rate limiting).

#### Données de test
Vous pouvez utiliser la liste suivante d’URLs (API publique disponible) :
``` 
const urls = [
"https://jsonplaceholder.typicode.com/todos/1",
"https://jsonplaceholder.typicode.com/todos/2",
"https://jsonplaceholder.typicode.com/todos/3",
"https://jsonplaceholder.typicode.com/todos/4",
"https://jsonplaceholder.typicode.com/todos/5"];
``` 
#### Chaque URL retourne un objet JSON au format suivant :
``` 
{"userId": 1,"id": 1,"title": "exemple","completed": false }
``` 
#### Exemple d’utilisation attendue
``` 
fetchUrls(urls).then(console.log);
``` 
#### Résultat attendu (ordre respecté) :
``` 
[{ "userId": 1, "id": 1, "title": "...", "completed": false },{ "userId": 1, "id": 2, "title": "...", "completed": false },{ "userId": 1, "id": 3, "title": "...", "completed": false },{ "userId": 1, "id": 4, "title": "...", "completed": true },{ "userId": 1, "id": 5, "title": "...", "completed": false } ]
``` 

 