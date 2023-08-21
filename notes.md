JavaScript propose un grand nombre de fonctions intégrées pour effectuer différentes tâches. Voici une liste de fonctions couramment utilisées avec des exemples :

1. **Fonctions de sortie (affichage) :**
   - `console.log()`: Affiche des informations dans la console du navigateur.
     ```javascript
     console.log("Hello, world!");
     ```

2. **Fonctions de manipulation de chaînes :**
   - `String.length`: Retourne la longueur d'une chaîne.
     ```javascript
     const message = "Hello, world!";
     console.log(message.length); // Affiche 13
     ```

   - `String.toUpperCase()` et `String.toLowerCase()`: Convertit une chaîne en majuscules ou en minuscules.
     ```javascript
     const text = "Hello";
     console.log(text.toUpperCase()); // Affiche "HELLO"
     console.log(text.toLowerCase()); // Affiche "hello"
     ```

   - `String.indexOf()` et `String.lastIndexOf()`: Recherche la position d'un sous-ensemble dans une chaîne.
     ```javascript
     const sentence = "This is a sample sentence.";
     console.log(sentence.indexOf("is")); // Affiche 2
     console.log(sentence.lastIndexOf("is")); // Affiche 5
     ```

3. **Fonctions mathématiques :**
   - `Math.random()`: Génère un nombre décimal aléatoire entre 0 (inclus) et 1 (exclus).
     ```javascript
     const randomNum = Math.random();
     console.log(randomNum);
     ```

   - `Math.floor()`, `Math.ceil()` et `Math.round()`: Arrondissent des nombres vers le bas, le haut ou au nombre entier le plus proche.
     ```javascript
     console.log(Math.floor(3.8)); // Affiche 3
     console.log(Math.ceil(3.2));  // Affiche 4
     console.log(Math.round(3.5)); // Affiche 4
     ```

   - `Math.max()` et `Math.min()`: Trouvent le plus grand ou le plus petit nombre d'une série.
     ```javascript
     console.log(Math.max(5, 2, 8)); // Affiche 8
     console.log(Math.min(5, 2, 8)); // Affiche 2
     ```

4. **Fonctions de manipulation d'objets et de tableaux :**
   - `Array.isArray()`: Vérifie si une variable est un tableau.
     ```javascript
     const myArray = [1, 2, 3];
     console.log(Array.isArray(myArray)); // Affiche true
     ```

   - `Array.push()` et `Array.pop()`: Ajoutent ou suppriment un élément à la fin d'un tableau.
     ```javascript
     const numbers = [1, 2, 3];
     numbers.push(4);
     console.log(numbers); // Affiche [1, 2, 3, 4]
     numbers.pop();
     console.log(numbers); // Affiche [1, 2, 3]
     ```

   - `Array.join()`: Convertit un tableau en une chaîne en joignant les éléments avec un séparateur.
     ```javascript
     const fruits = ["apple", "banana", "orange"];
     const fruitString = fruits.join(", ");
     console.log(fruitString); // Affiche "apple, banana, orange"
     ```

5. **Fonctions de manipulation de dates :**
   - `Date()`: Crée un nouvel objet de date représentant l'heure actuelle.
     ```javascript
     const currentDate = new Date();
     console.log(currentDate);
     ```

   - `Date.getFullYear()`, `Date.getMonth()`, `Date.getDate()`, etc. : Retournent les éléments de la date (année, mois, jour, etc.).
     ```javascript
     const now = new Date();
     console.log(now.getFullYear()); // Affiche l'année actuelle
     console.log(now.getMonth());    // Affiche le mois actuel (0-11)
     console.log(now.getDate());     // Affiche le jour actuel (1-31)
     ```

Ceci n'est qu'un aperçu de quelques fonctions JavaScript. Il en existe beaucoup plus pour accomplir une variété de tâches, allant de la manipulation du DOM à la gestion des événements et bien plus encore.

Manipuler le Document Object Model (DOM) est une part importante de la programmation en JavaScript pour interagir avec les éléments d'une page web. Voici une liste de fonctions JavaScript couramment utilisées pour manipuler le DOM, accompagnées d'exemples :

1. **Sélection d'éléments :**
   - `document.getElementById(id)`: Sélectionne un élément par son ID.
     ```javascript
     const elementById = document.getElementById('myElement');
     ```

   - `document.querySelector(selector)`: Sélectionne le premier élément qui correspond au sélecteur CSS.
     ```javascript
     const firstParagraph = document.querySelector('p');
     ```

   - `document.querySelectorAll(selector)`: Sélectionne tous les éléments qui correspondent au sélecteur CSS.
     ```javascript
     const allParagraphs = document.querySelectorAll('p');
     ```

2. **Modification de contenu :**
   - `.textContent`: Modifie ou accède au contenu textuel d'un élément.
     ```javascript
     const element = document.getElementById('myElement');
     element.textContent = 'Nouveau contenu';
     ```

   - `.innerHTML`: Modifie ou accède au contenu HTML d'un élément.
     ```javascript
     const element = document.getElementById('myElement');
     element.innerHTML = '<strong>Texte en gras</strong>';
     ```

3. **Modification des attributs :**
   - `.setAttribute(name, value)`: Définit la valeur d'un attribut pour un élément.
     ```javascript
     const link = document.querySelector('a');
     link.setAttribute('href', 'https://example.com');
     ```

   - `.getAttribute(name)`: Récupère la valeur d'un attribut d'un élément.
     ```javascript
     const link = document.querySelector('a');
     const hrefValue = link.getAttribute('href');
     ```

4. **Ajout et suppression d'éléments :**
   - `document.createElement(tagName)`: Crée un nouvel élément avec le nom de balise spécifié.
     ```javascript
     const newElement = document.createElement('div');
     ```

   - `.appendChild(child)`: Ajoute un élément comme enfant d'un autre élément.
     ```javascript
     const parentElement = document.getElementById('parent');
     parentElement.appendChild(newElement);
     ```

   - `.removeChild(child)`: Supprime un enfant d'un élément parent.
     ```javascript
     const parentElement = document.getElementById('parent');
     const childElement = document.getElementById('child');
     parentElement.removeChild(childElement);
     ```

5. **Classes CSS :**
   - `.classList.add(className)`: Ajoute une classe à un élément.
     ```javascript
     const element = document.getElementById('myElement');
     element.classList.add('highlight');
     ```

   - `.classList.remove(className)`: Supprime une classe d'un élément.
     ```javascript
     const element = document.getElementById('myElement');
     element.classList.remove('highlight');
     ```

6. **Événements :**
   - `.addEventListener(event, callback)`: Attache un écouteur d'événement à un élément.
     ```javascript
     const button = document.getElementById('myButton');
     button.addEventListener('click', () => {
         console.log('Le bouton a été cliqué.');
     });
     ```

Ces exemples illustrent quelques-unes des fonctions JavaScript les plus couramment utilisées pour manipuler le DOM. N'oubliez pas que le DOM offre de nombreuses autres fonctionnalités et méthodes pour une manipulation plus avancée et ciblée des éléments sur une page web.


Ces méthodes permettent de manipuler les tableaux de manière efficace et expressive. N'hésitez pas à les combiner pour réaliser des opérations plus complexes sur les tableaux en JavaScript.

Bien sûr, voici des exemples concrets d'utilisation de certaines des méthodes de tableau mentionnées :

En JavaScript, les tableaux possèdent plusieurs méthodes intégrées qui permettent de manipuler, filtrer, parcourir et modifier leurs éléments. Voici une liste de certaines des méthodes les plus couramment utilisées qui s'appliquent sur tous les tableaux :

1. **Ajout et suppression d'éléments :**
   - `.push(element)`: Ajoute un élément à la fin du tableau.
   - `.pop()`: Supprime le dernier élément du tableau.
   - `.shift()`: Supprime le premier élément du tableau.
   - `.unshift(element)`: Ajoute un élément au début du tableau.

1. **Ajout et suppression d'éléments :**
```javascript
let numbers = [1, 2, 3];

numbers.push(4); // Ajoute 4 à la fin du tableau
console.log(numbers); // Affiche [1, 2, 3, 4]

numbers.pop(); // Supprime le dernier élément (4)
console.log(numbers); // Affiche [1, 2, 3]

numbers.shift(); // Supprime le premier élément (1)
console.log(numbers); // Affiche [2, 3]

numbers.unshift(0); // Ajoute 0 au début du tableau
console.log(numbers); // Affiche [0, 2, 3]
```

2. **Parcours et itération :**
   - `.forEach(callback)`: Exécute une fonction sur chaque élément du tableau.
   - `.map(callback)`: Crée un nouveau tableau en appliquant une fonction à chaque élément.
   - `.filter(callback)`: Crée un nouveau tableau avec les éléments qui satisfont une condition.
   - `.find(callback)`: Renvoie le premier élément qui satisfait une condition.
   - `.indexOf(element)`: Renvoie l'index du premier élément correspondant.
   - `.lastIndexOf(element)`: Renvoie l'index du dernier élément correspondant.


2. **Parcours et itération :**
```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((number) => {
    console.log(number); // Affiche chaque nombre du tableau
});

const squaredNumbers = numbers.map((number) => {
    return number * number; // Crée un nouveau tableau avec les carrés des nombres
});
console.log(squaredNumbers); // Affiche [1, 4, 9, 16, 25]

const evenNumbers = numbers.filter((number) => {
    return number % 2 === 0; // Crée un nouveau tableau avec les nombres pairs
});
console.log(evenNumbers); // Affiche [2, 4]

const firstEvenNumber = numbers.find((number) => {
    return number % 2 === 0; // Trouve le premier nombre pair (2)
});
console.log(firstEvenNumber); // Affiche 2

const indexOfThree = numbers.indexOf(3); // Trouve l'index de 3 (2)
console.log(indexOfThree); // Affiche 2
```
3. **Vérification et manipulation :**
   - `.includes(element)`: Vérifie si le tableau contient un élément donné.
   - `.some(callback)`: Vérifie si au moins un élément satisfait une condition.
   - `.every(callback)`: Vérifie si tous les éléments satisfont une condition.
   - `.sort(compareFunction)`: Trie les éléments du tableau (peut être utilisé avec une fonction de comparaison personnalisée).
   - `.reverse()`: Inverse l'ordre des éléments dans le tableau.


3. **Vérification et manipulation :**
```javascript
const fruits = ['apple', 'banana', 'orange'];

console.log(fruits.includes('banana')); // true
console.log(fruits.some(fruit => fruit === 'apple')); // true
console.log(fruits.every(fruit => fruit.length > 3)); // true

fruits.sort(); // Trie les fruits par ordre alphabétique
console.log(fruits); // Affiche ['apple', 'banana', 'orange']

fruits.reverse(); // Inverse l'ordre des fruits
console.log(fruits); // Affiche ['orange', 'banana', 'apple']
```
4. **Réduction (agrégation) :**
   - `.reduce(callback, initialValue)`: Applique une fonction de réduction sur les éléments du tableau pour obtenir une valeur unique.
   - `.reduceRight(callback, initialValue)`: Même que `reduce`, mais en commençant par la fin du tableau.

4. **Réduction (agrégation) :**
```javascript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => {
    return accumulator + currentValue; // Calcule la somme des nombres
}, 0);
console.log(sum); // Affiche 15
```

5. **Transformation :**
   - `.join(separator)`: Crée une chaîne en joignant les éléments du tableau avec le séparateur spécifié.
   - `.slice(start, end)`: Crée un nouveau tableau en extrayant une portion du tableau original.
   - `.splice(start, deleteCount, ...items)`: Modifie le tableau en supprimant/remplaçant/ajoutant des éléments à partir de l'index spécifié.


5. **Transformation :**
```javascript
const words = ['Hello', 'world', 'how', 'are', 'you'];

const sentence = words.join(' '); // Crée une phrase avec des espaces
console.log(sentence); // Affiche "Hello world how are you"

const subArray = words.slice(1, 3); // Crée un sous-tableau avec 'world' et 'how'
console.log(subArray); // Affiche ['world', 'how']
```
6. **Vérification de type :**
   - `.isArray()`: Vérifie si une variable est un tableau.

6. **Vérification de type :**
```javascript
const myArray = [1, 2, 3];

console.log(Array.isArray(myArray)); // true
```
7. **Copie et clonage :**
   - `.concat(...arrays)`: Fusionne plusieurs tableaux pour créer un nouveau tableau.
   - `.slice()`: Crée une copie superficielle (shallow copy) du tableau.

8. **Transformations :**
   - `.map(callback)`: Crée un nouveau tableau en appliquant une fonction à chaque élément.
   - `.flatMap(callback)`: Crée un nouveau tableau en appliquant une fonction à chaque élément et en aplatissant les résultats.

Ces exemples illustrent différentes méthodes pour manipuler les tableaux en JavaScript. Vous pouvez les combiner de différentes manières pour accomplir des tâches spécifiques en fonction de vos besoins.

