# Polymorphism & Composition Homework - Quiz

# Polymorphism

<details>
<summary>1. What does the <em>word</em>  'polymorphism' mean?</summary>
It means "having more than one shape", coming from the Greek πολύμορϕος (πολυ- "multiple-" and μορϕή "shape").
</details>

<details>
<summary>2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.</summary>
It means that the objects of a class will have the behaviour (eg. the properties and the methods) of more than one class, more specifically its own plus the ones of its parent class. Polymorphism can in fact only be applied when we have a child class inheriting the properties of the parent class, and establishes a "is-a" relationship between classes. For example, if we have the class <code>HybridCar</code> and a parent class <code>Car</code>, the <code>HybridCar</code>'s instances will be inheriting all the variables and the methods belonging to its parent class <code>Car</code> as <code>HybridCar</code> "is a" <code>Car</code>.
</details>

<details>
<summary>3. What can we use to implement polymorphism in Java?</summary>
We can use both abstract classes and interfaces: interfaces are preferable as they are lighter and more easily usable than inheritance.
</details>

<details>
<summary>4. How many 'forms' can an object take when using polymorphism?</summary>
It can have as many shapes as the number of classes from which it inherits, being them related "genealogically" (eg. the class is inheriting from its parent class and from the grand parent class, from which the parent class is inheriting primarily) or by interface.
</details>

<details>
<summary>5. Give an example of when you could use polymorphism.</summary>
Task: create a paddock that includes horses and unicorns.
We could create the <code>Horse</code> and <code>Unicorn</code> classes, where <code>Unicorn</code> inherits from <code>Horse</code>, then create an ArrayList of Horses that includes both classes. We can only include both in the same array because <code>unicorn</code> is both an instance of <code>Unicorn</code> and a type of <code>Horse</code>, and each <code>unicorn</code> "is-a" <code>horse</code>. The opposite (all horses are unicorns) is not valid.

```
// HORSE CLASS

public class Horse {
  private String maneColour:
  private int numberOfHooves;

  public Horse(String maneColour, int numberOfHooves) {
    this.maneColour = maneColour;
    this.numberOfHooves = numberOfHooves;
  }

  public String getManeColour() {
    return maneColour;
  }

  public int getNumberOfHooves() {
    return numberOfHooves;
  }
}


// UNICORN CLASS

public class Unicorn extends Horse{

  private int numberOfHorns;

  public Unicorn(String maneColour, int numberOfHooves,  int numberOfHorns) {
    super(maneColour, numberOfHooves);
    this.numberOfHorns =  int numberOfHorns;
  }

  public String getNumberOfHorns() {
    return numberOfHorns;
  }
}


// PADDOCK CLASS
[...]

  ArrayList<Horse> paddockHorses= new ArrayList<>();
    Horse sandy = new Horse ("black", 4);
    Horse pie = new Horse ("blonde", 4);
    Horse furious = new Horse ("brown", 4);
    Unicorn rainbow = new Unicorn ("rainbow", 4, 1);
    Unicorn skye = new Unicorn ("white", 4, 1);

    paddockHorses.add(sandy);
    paddockHorses.add(pie);
    paddockHorses.add(furious);
    paddockHorses.add(rainbow);
    paddockHorses.add(skye);
```
</details>



# Composition

<details>
<summary>6. What do we mean by 'composition' in reference to object-oriented programming?</summary>
We mean that the objects of a class will have the behaviour of another class, allowing the first to reuse the second's code. It establishes a "has-a" relationship between classes.
</details>

<details>
<summary>7. When would you use composition? Provide a simple example in Java.</summary>
Task: create a cupboard.  
To create the class <code>Cupboard</code> we could create each component of the cupboard as a single class, ie <code>Door</code>, <code>Handler</code>, <code>Shelf</code>, <code>Panel</code> and use them as instance variables of the class <code>Cupboard<code>. We can see at that point how the <code>Cupboard<code> "has-a" <code>Door</code>, <code>Handler</code>, <code>Shelf</code>, <code>Panel</code>.
</details>

<details>
<summary>8. What is/are the advantage(s) of using composition?
</summary>
The advantages of using composition are that:
* there is no need to override methods in the composed class;  
* it allows the composed class to accept as many classes as needed;  
* the composed class is not intaking unnecessary behaviours from its ancestors;  
* the composed class is not polluted by unnecessary coding (ie duplicated methods coming from different classes just to achieve having only some of those classes behaviours).
</details>

<details>
<summary>9. When an object is destroyed, what happens to all the objects it is composed of?</summary>
They are destroyed.
</details>
