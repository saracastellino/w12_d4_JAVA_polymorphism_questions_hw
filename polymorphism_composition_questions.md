# Polymorphism & Composition Homework - Quiz

# Polymorphism

<details>
<summary>1. What does the word 'polymorphism' mean?</summary>
<p>It means "having more than one shape", coming from the Greek πολύμορϕος (πολυ- "multiple-" and μορϕή "shape").</p>
</details>

<details>
<summary>2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.</summary>
<p>It means that the objects of a class will have the behaviour (eg. the properties and the methods) of more than one class, more specifically its own plus the ones of its parent class. Polymorphism can in fact only be applied when we have a child class inheriting the properties of the parent class, and establishes a "is-a" relationship between classes. For example, if we have the class HybridCar and a parent class Car, the HybridCar's instances will be inheriting all the variables and the methods belonging to its parent class Car.</p>
</details>

<details>
<summary>3. What can we use to implement polymorphism in Java?</summary>
<p>We can use both abstract classes and interfaces: interfaces are preferable as they are lighter and more easily usable than inheritance.</p>
</details>

<details>
<summary>4. How many 'forms' can an object take when using polymorphism?</summary>
<p>It can have as many shapes as the number of classes from which it inherits, being them related "genealogically" (eg. the class is inheriting from its parent class and from the grand parent class, from which the parent class is inheriting primarily) or by interface.</p>
</details>

<details>
<summary>5. Give an example of when you could use polymorphism.</summary>
<p>Task: create a paddock that includes horses and unicorns.
We could create the Horse and Unicorn classes, where Unicorn inherits from Horse, then create an ArrayList of Horses that includes both classes. We can only include both in the same array because Unicorn is both an instance of Unicorn and a type of Horse. The opposite (all horses are unicorns) is not valid.</p>

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
<p>We mean that the objects of a class will have the behaviour of another class, allowing the first to reuse the second's code. It establishes a "has-a" relationship between classes.</p>
</details>

<details>
<summary>7. When would you use composition? Provide a simple example in Java.</summary>
<p>It means that the objects of a class will have the behaviour (eg. the properties and the methods) of more than one class, more specifically its own plus the ones of its parent class. Polymorphism can in fact only be applied when we have a child class inheriting the properties of the parent class. For example, if we have the class HybridCar and a parent class Car, the HybridCar's instances will be inheriting all the variables and the methods belonging to its parent class Car.</p>
</details>

<details>
<summary>8. What is/are the advantage(s) of using composition?
</summary>
<p>It means that the objects of a class will have the behaviour (eg. the properties and the methods) of more than one class, more specifically its own plus the ones of its parent class. Polymorphism can in fact only be applied when we have a child class inheriting the properties of the parent class. For example, if we have the class HybridCar and a parent class Car, the HybridCar's instances will be inheriting all the variables and the methods belonging to its parent class Car.</p>
</details>

<details>
<summary>9. When an object is destroyed, what happens to all the objects it is composed of?<details></summary>
<p>It means that the objects of a class will have the behaviour (eg. the properties and the methods) of more than one class, more specifically its own plus the ones of its parent class. Polymorphism can in fact only be applied when we have a child class inheriting the properties of the parent class. For example, if we have the class HybridCar and a parent class Car, the HybridCar's instances will be inheriting all the variables and the methods belonging to its parent class Car.</p>
</details>
