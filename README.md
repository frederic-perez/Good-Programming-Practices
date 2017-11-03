# Good-Programming-Practices

<p align="center">
  <img src="images/always-code-as-if-the-guy-who-ends-up-maintaining--400x200.jpg?raw=true" alt="Martin Golding quote"/>
</p>

- _"Writing clean code is what you must do in order to call yourself a professional. There is no reasonable excuse for doing anything less than your best."_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
- _"We feel that there is no point in developing software unless you care about doing it well."_ -- Andrew Hunt, David Thomas, _The Pragmatic Programmer: From Journeyman to Master_

## Principles of Software Development

- From STUPID to SOLID code ([slides](http://slides.williamdurand.fr/from-stupid-to-solid-code/#/) by [William Durand](http://williamdurand.fr/))
  - STUPID
    - Singleton
    - Tight Coupling
    - Untestability
    - Premature Optimization
    - Indescriptive Naming
    - Duplication, also known as __WET__ (We Edit Terribly, We Enjoy Typing...) _vs_ the recommended __DRY__ (Don't Repeat Yourself)
  - [SOLID](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design))
    > Acronym for five design principles intended to make software designs more understandable, flexible and maintainable.

    - [Single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle)
      > A class should have only a single responsibility (i.e. changes to only one part of the software's specification should be able to affect the specification of the class).
      > [...] The reason it is important to keep a class focused on a single concern is that it makes the class _more robust_.
    - [Open/closed principle](https://en.wikipedia.org/wiki/Open/closed_principle)
      > “Software entities ... should be open for extension, but closed for modification.”
    - [Liskov substitution principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle)
      > “Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.”
    - [Interface segregation principle](https://en.wikipedia.org/wiki/Interface_segregation_principle)
      > “Many client-specific interfaces are better than one general-purpose interface.”
    - [Dependency inversion principle](https://en.wikipedia.org/wiki/Dependency_inversion_principle)
      > "One should “depend upon abstractions, [not] concretions"

## Unit Testing

### Frameworks

- [List of unit testing frameworks](https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks)
- Google Mock, the Google C++ mocking framework
  - :octocat: [googlemock](https://github.com/google/googletest/tree/master/googlemock)
  - [README.md](https://github.com/google/googletest/blob/master/googlemock/README.md)
  - [CheatSheet](https://github.com/google/googletest/blob/master/googlemock/docs/CheatSheet.md)
  - [CookBook](https://github.com/google/googletest/blob/master/googlemock/docs/CookBook.md)
- [GUnit](https://github.com/cpp-testing/GUnit), GoogleTest/GoogleMock/Cucumber on steroids, by Kris Jusiak

### Principles++

- [Given-When-Then (GWT)](https://en.m.wikipedia.org/wiki/Given-When-Then),
  [Four-Phase Test](http://xunitpatterns.com/Four%20Phase%20Test.html),
  [Arrange-Act-Assert (AAA)](http://wiki.c2.com/?ArrangeActAssert)

  - From [Martin Fowler's article](https://martinfowler.com/bliki/GivenWhenThen.html):
    >  It's an approach developed by Dan North and Chris Matts as part of BDD. [...] You can also look at it as a reformulation of the Four-Phase Test pattern.

    Four-Phase Test pattern: 1. Setup 2. Execute 3. Check 4. Teardown

    |   | GWT   | Four Ph. | AAA
    | - | :---: |:--------:| :-:
    | 1 | Given | Setup    | Arrange
    | 2 | When  | Execute  | Act
    | 3 | Then  | Check    | Assert
    | 4 |       | Teardown |

  - Example of the naming convention introduced to me by [Angel Costela](https://www.linkedin.com/in/angel-costela-sanmiguel-b84229a6/):  __Given__\_state\__A_\___When__\__B_\_happens\___Then__\_these\_conditions\_must\_be\_met\()

  - Example (written as pseudo-code):
    ```c++
    void Given_state_A_When_B_happens_Then_these_conditions_must_be_met() {
      set_state_A();                      // Given | Setup    | Arrange
      B();                                // When  | Execute  | Act
      assert(condition_1 and condition2); // Then  | Check    | Assert
      ;                                   //       | Teardown |
    }
    ```

- From _C++Now 2017_, Kris Jusiak's “Towards Painless Testing" [(video)](https://www.youtube.com/watch?v=NVrZjT5lW5o) (published on Jun 13, 2017)

### First and foremost: Compilers and static analyzers are our friends

#### Compilers, not compiler

#### Zero compiler warnings policy

The first tool against software bugs, perhaps right after writing clean code, and right before using static analyzers, should be using adequate compiler(s) warning flags, and achieving zero warnings. During my career I've suffered time and again bugs in production very hard to pinpoint that could have been eradicated simply by taking care of compiler warnings. This has a high cost in time and money, in addition to experiencing a high level of frustration.

It is important to point out that the goal is not simply "get rid of the warning" (or, in other words, "satisfy the compiler"), but to actually fix the code. In the past I've seen "fixes" to satisfy the compiler that actually introduced bugs--not a good tradeoff!

#### Preventive coding

Whenever possible, take advantage of __static assertions__ to discover coding problems at the compilation stage. In C++ I'm also an advocate of extensive use of the keyword `const`, and, from C++11, forbid `NULL` favoring `nullptr` instead.

#### Static analyzers

I'm a huge fan of [Cppcheck](http://cppcheck.sourceforge.net/), since it has helped me identifying coding bugs which could have slipped through. These coding bugs were sometimes, but _not always_, also detected by the compiler as warnings or even errors!

## Incomplete list of favorite gurus

Sort of alphabetically sorted:

- Andrew Sutton: :octocat: [asutton](https://github.com/asutton)
- Bjarne Stroustrup
- Herb Sutter
- Jason Turner: :octocat: [lefticus](https://github.com/lefticus)
- Kent Beck
- Krzysztof/Kris Jusiak: :octocat: [krzysztof-jusiak](https://github.com/krzysztof-jusiak), [kris.jusiak.net](http://kris.jusiak.net/)
- Robert C. Martin
- Scott Meyers

## List of selected great books

- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
  - Notes on GitHub: [jbarroso/clean-code](https://github.com/jbarroso/clean-code)
- Robert C. Martin, _Agile Software Development, Principles, Patterns, and Practices_
