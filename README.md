# Architect form hell (meta-)Kata

This kata is about code and management. It is based on the [Kebab Kata](https://github.com/malk/the-kebab-kata) by [Romeu Moura](https://twitter.com/malk_zameth). The purpose is to make people reflects about both absurd (well... inefficient) but realistic decisions taken by a single figure of authority, who doesn't show any empathy.

Time: 1h = code/RPG 40mn + 20mn retrospective

This kata can be played during a code retreat. If so, think about playing it after the second iteration.

In this kata, the attendees play the role of the developers and the facilitator plays the role of the architect from hell.

# Preparation

* First you must choose a code kata too long for 40mn
* Design an inefficient architecture for the problem
* Make the UML diagram of this architecture
* Think up adding a new feature in your architecture or changing a way to implement an existing one
* Repeat your role

# The Kata

## Introduction

* Tell the attendees that the kata is going to be somewhat hard emotionally. But we'll, it's only 40mn long.
* Tell them that there will be a retrospective :)
* Devs should work in pair

## Introduction of the ARCHITECT

* Change your mind! Change your voice tone! You are THE ARCHITECT.
* Introduce yourself as Bob (or your name). You're the new architect and you will help the dev team to deliver on time. Here, attendees must perceived hope. Be smiling, it helps ;)
* False hope!

> I've discussed with business people and design with them the architecture of the application.

* Show the UML diagram to the devs and indicate that you won't explain the choices as it'll be too difficult for them to understand
* On a specific part of the diagram, indicate that the implementation as been decided by the business people

## Iteration 1

* Give them 30mn to code and indicate that there will be a demo and a code review by peer
* You are allowed to answer questions ;)
* 15mn later, tell then:

> The business has detected an opportunity and we need to deliver earlier. Demo in 5mn.

* For each pair, ask for a demo (they have to explain their code). Be smilling, say OK regularly, but inside you have to be uninteressed and go quickly to the next pair
* Every two pairs visited asked to exchange a pair for code review
* After 2mn max, stop the review and launch the second iteration

## Iteration 2

* Tell to all devs that you are disappointed by the work done (don't hesitate to evaluate each pair for whatever reason. Eg. "for you, it wast OK", "you, you've asked me some questions and it's something I dislike". Only do quick comments.)

> I let you another chance. I've just talked with the business. They have detected another opportunity. This let you time to finish the work. But you also have to add a small modification, that has been decided by the business.

* Show the change in architecture directly on the UML diagram

 > You have 10mn to finish the job!

* 10mn later, ask each pair for a demo with the same mood than in the previous iteration.

## Retrospective (20mn)

* Here, you stop being the architect from hell!
* Ask everybody to join you in front of a board
* Ask each one to express what they felt during the session (this is important!)
* List all the things on the board
* Then, ask to find ideas about what they could do to make things better

# Example with the Conway's Game of Life

```java
public interface Cell {
  int getX();
  int getY();

  boolean isAlive();
  int countAliveCellsAround();
}

public class AliveCell implements Cell { /* TODO */ }
public class DeadCell implements Cell { /* TODO */ }

public class Grid {
  /* A grid is a cell container (dead or alive)
   * - iteration #1: devs should use a matrix (array of arrays) to represent the grid
   * - iteration #2: devs should use a set (#java.util.Set) to represent the grid (and yes, they have to put every kind of cell in, dead or alive)
   */

   // TODO
}
```
