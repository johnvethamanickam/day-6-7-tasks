1. The class Movie is stated below. An instance of class Movie represents a film. This class has the following three properties:

-   title, which is a String representing the title of the movie
-   studio, which is a String representing the studio that made the movie
-   rating, which is a String representing the rating of the movie (i.e. PG­13, R, etc)

a) Write a constructor for the class Movie, which takes a String representing the title of the movie, a String representing the studio, and a String representing the rating as its arguments, and sets the respective class properties to these values.

b) The constructor for the class Movie will set the class property rating to "PG" as default when no rating is provided.

c) Write a method getPG, which takes an array of base type Movie as its argument, and returns a new array of only those movies in the input array with a rating of "PG". You may assume the input array is full of Movie instances. The returned array need not be full.

d) Write a piece of code that creates an instance of the class Movie with the title “Casino Royale”, the studio “Eon Productions”, and the rating “PG­13”

**a. Here's the constructor for the `Movie` class:**

```js
class Movie {  
  constructor() {  
    this.title = 'Paiya';  
    this.studio= 'Red jaint'  
    this.rating= 'PG 13'  
  }  
}  
  
const Movie1 = new Movie();  
  
console.log(Movie1.rating);

```

**b. In the constructor above, the rating property is set to "PG" as default when no rating is provided.**

```js
class Movie {  
  
 constructor(title, studio, rating) {  
 this.title = title;  
 this.studio= studio;  
 this.rating= rating;  
 if (rating != null) {
    this.rating = rating;
} else {
    this.rating = "PG";
}
 }  
    }  
    const Movie1 = new Movie("paiya", "red jaint");  
console.log(Movie1.rating);
        
```
**c. Here's the `getPG` method:**

```js
var movies= [{
  "title":"Harry Potter",
  "studio":"Warner Bros. Pictures",
  "rating":"PG"
  },
  {
  "title":"Avatar",
  "studio":"Nickelodeon Animation",
  "rating":"PG 13"
  },
  {
  "title":"Life of Pi",
  "studio":"Rhythm & Hues",
  "rating":"PG"
  }
]
  function getPG(movies) {
  const pgMovies = [];
  for (let i = 0; i < movies.length; i++) {
    if (movies[i].rating === 'PG') {
      pgMovies.push(movies[i].title);
    }
  }
  return pgMovies;  
}
const pgMovies = getPG(movies);
console.log(pgMovies);

```

**d. Here's the code to create an instance of `Movie` with the title "Casino Royale", the studio "Eon Productions", and the rating "PG-13" in JavaScript:**

```js
let movie = new Movie("Casino Royale", "Eon Productions", "PG-13");
 
```

2. 

```js
class Circle{
  constructor(radius, color){
    this.setRadius(radius);
    this.setColor(color);
  }
  setRadius(radius){
    this.radius = radius;
  }
  getRadius(){
    return this.radius;
  }
  setColor(color){
    this.color = color;
  }
  getColor(){
    return this.color;
  }
  getArea(){
     return this.area=Math.PI * this.radius * this.radius;
  }
  getCircumference(){
      return this.circumference=2* Math.PI * this.radius;
  }
}
let a=new Circle(2, "Red");
console.log(a.getRadius())
a.setRadius(5);
console.log(a.getRadius())
console.log(a.getArea());
console.log(a.getCircumference());

```

**3. Write a “person” class to hold all the details.**

```js
class Person {
  name;
  age;
  email;
  
  constructor(name, age, email) {
    this.name = name;
    this.age = age;
    this.email = email;
  }
}
let person = new Person("Nithish kumar", 24, "nithishkumar.17@hotmail.com");
  
console.log(person.name);
console.log(person.age);
console.log(person.email);
```

**4. write a class to calculate the uber price.**

```js
class Uber {
    constructor(distance, time) {
      this.distance = distance;
      this.time = time;
      this.baseFare = 40;
      this.costPerMile = 35;
      this.costPerMinute = 15;
      this.minimumFare = 80;
    }
    calculateFare() {
      const distanceCost = this.distance * this.costPerMile;
      const timeCost = this.time * this.costPerMinute;
      const fare = this.baseFare + distanceCost + timeCost;
      return fare < this.minimumFare ? this.minimumFare : fare;
    }
  }
let ride = new Uber(10, 25);
console.log(ride.calculateFare());
```
