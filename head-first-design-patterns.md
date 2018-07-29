---
description: 'My notes and exercises from the book: Head First Design Patterns'
---

# Head First Design Patterns

> Current Page: 15

View the book online [here](./resources/Head-First-Design-Patterns-[2004].pdf).

# Chapter 1

## Design Principles

1. [Page 9] Identify the aspects of your application that vary and separate them from what stays the same.
2. [Page 11] Program to an interface, not an implementation.

## Page 8 - Exercies

Lots of things can drive change. List some reasons you’ve had to change code in your applications.

- To improve DX (developer experience) and ease of feature implementation.
- Fixing bugs that span across large portions of the code base.
- A new feature requires different build process to enable new features that the old code doesn't support.

## Page 14 - Questions

Q1. Do I always have to implement my application first, see where things are changing, and then go back and separate & encapsulate those things?
A1. Not always, you could abstract the implementation early on if you are aware that eventually new features will need to be added.

Q2. Should we make Duck an interface too?
A2. No. We want to have a base class that we can extend from which has generic implementation logic. The other Duck types have the specifics backed into them based on the behaviours they need to have.

Q3. It feels a little weird to have a class that’s just a behavior. Aren’t classes supposed to represent things? Aren’t classes supposed to have both state AND behavior?
A3. It's fine to separate behaviour from state as it may make sense to share the behaviour across many different classes. The state can be kept within the class that implements the behaviour so there is not really any issue here that I can see.

Q4. Using our new design, what would you do if you needed to add rocket-powered flying to the SimUDuck app?
A4. I would extend the Flying class behaviour to have another method called rocketPowered()
E4. Create a FlyRocketPowered class that implements the FlyBehavior interface

Q5. Can you think of a class that might want to use the Quack behavior that isn’t a duck?
A5. Nope.
E5. One example, a duck call (a device that makes duck sounds)