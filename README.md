# Good-Programming-Practices

<p align="center">
  <img src="images/always-code-as-if-the-guy-who-ends-up-maintaining--400x200.jpg?raw=true" alt="Martin Golding quote"/>
</p>

- _"Writing clean code is what you must do in order to call yourself a professional. There is no reasonable excuse for doing anything less than your best."_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
- _"We feel that there is no point in developing software unless you care about doing it well."_ -- Andrew Hunt, David Thomas, _The Pragmatic Programmer: From Journeyman to Master_

## Principles of Software Development

- DRY (Don't Repeat Yourself) vs WET (We Edit Terribly, We Enjoy Typing...)
- [SOLID](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design))
  > acronym for five design principles intended to make software designs more understandable, flexible and maintainable.

  - S: [Single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle)
    > a class should have only a single responsibility (i.e. changes to only one part of the software's specification should be able to affect the specification of the class)
  - O: [Open/closed principle](https://en.wikipedia.org/wiki/Open/closed_principle)
    > “software entities ... should be open for extension, but closed for modification.”
  - L: [Liskov substitution principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle)
    > “objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.”
  - I: [Interface segregation principle](https://en.wikipedia.org/wiki/Interface_segregation_principle)
    > “many client-specific interfaces are better than one general-purpose interface.”
  - D: [Dependency inversion principle](https://en.wikipedia.org/wiki/Dependency_inversion_principle)
    > one should “depend upon abstractions, [not] concretions"

## To be classified

- TDD
- BDD
- XP
- Unit Testing
  - Great naming convention by Angel Costela:  __Given__\_state\_a\___When__\_b\_happens\___Then__\_return\_{true|false|...}

### First and foremost: Zero compiler warnings policy

The first tool against software bugs, perhaps right after writing clean code, and right before using static analyzers, should be using adequate compiler(s) warning flags, and achieving zero warnings. During my career I've suffered time and again bugs in production very hard to pinpoint that could have been eradicated simply by taking care of compiler warnings. This has a high cost in time and money, in addition to experiencing a high level of frustration.

It is important to point out that the goal is not simply "get rid of the warning" (or, in other words, "satisfy the compiler"), but to actually fix the code. In the past I've seen "fixes" to satisfy the compiler that actually introduced bugs--not a good tradeoff!

## Incomplete list of favorite gurus

Sort of alphabetically sorted:

- Andrew Sutton: GitHub: [asutton](https://github.com/asutton)
- Bjarne Stroustrup
- Herb Sutter
- Jason Turner: GitHub: [lefticus](https://github.com/lefticus)
- Kent Beck
- Robert C. Martin
- Scott Meyers

## List of selected great books

- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
  - Notes on GitHub: [jbarroso/clean-code](https://github.com/jbarroso/clean-code)
- Robert C. Martin, _Agile Software Development, Principles, Patterns, and Practices_

## Miscellany

### TODO

- Move stuff from ABcb here?
- Cost of a bug image?
- Copy stuff from my GTD files plus my old programming practices presentation?