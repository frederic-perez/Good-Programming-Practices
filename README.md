# Good-Programming-Practices

<p align="center">
  <img src="images/always-code-as-if-the-guy-who-ends-up-maintaining--400x200.jpg?raw=true" alt="Martin Golding quote"/>
</p>

First of all, a few very important related topics (at least to me):

- [Manifesto for Agile Software Development](https://www.smartsheet.com/comprehensive-guide-values-principles-agile-manifesto) (AKA “the Agile Manifesto”)

  - [The Four Values](https://agilemanifesto.org/) of the Agile Manifesto
  - [The Twelve Principles](https://agilemanifesto.org/principles.html) of the Agile Manifesto

- [Servant leadership](https://en.wikipedia.org/wiki/Servant_leadership) philosophy ([article](https://expertprogrammanagement.com/2018/04/servant-leadership/) in the Expert Program Management site)

- Avoiding a low [bus factor](https://en.wikipedia.org/wiki/Bus_factor)

Some great reminders:

- On __Professionalism__:

  - _“Writing clean code is what you must do in order to call yourself a professional. There is no reasonable excuse for doing anything less than your best.”_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_

  - _“We feel that there is no point in developing software unless you care about doing it well.”_ -- Andrew Hunt, David Thomas, _The Pragmatic Programmer: From Journeyman to Master_

- On __Bad Code__ and __Good Code__:

  - _“It was the bad code that brought the company down.”_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
  - _“Code is like humor. When you have to explain it, it’s bad.”_ -- Cory House
  - _“... good code matters ...”_ -- Kent Beck, _Implementation Patterns_

- On __Technical Debt__:

  - _“Later equals never.”_ -- LeBlanc’s law.

- On __Performance Management Objectives__:

  - _“Measuring programming progress by lines of code is like measuring aircraft building progress by weight.”_ -- Bill Gates

## Software Quality

- [Wikipedia entry on Software quality](https://en.wikipedia.org/wiki/Software_quality)

## Principles of Software Development

- From STUPID code to SOLID code ([slides](https://slides.williamdurand.fr/from-stupid-to-solid-code/#/) by [William Durand](https://williamdurand.fr/))
  - STUPID code
    - __S__: Singleton > [I.3](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Ri-singleton): Avoid singletons
    - __T__: Tight Coupling
    - __U__: Untestability
    - __P__: Premature Optimization
    - __I__: Indescriptive Naming (and just Naming, for that matter)
      > _“Choosing good names takes time but saves more than it takes. So take care with your names and __change them__ when you find better ones.”_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
      <!-- -->
      > _“You should name a variable using the same care with which you name a ﬁrst-born child.”_ -- James O. Coplien, in the Foreword of Robert C. Martin’s _Clean Code: A Handbook of Agile Software Craftsmanship_
    - __D__: Duplication, also known as __WET__ (We Edit Terribly, We Enjoy Typing...) _vs_ the recommended __DRY__ ([Don’t Repeat Yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself))
  - [SOLID](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)) code
    > Acronym for five design principles intended to make software designs more understandable, flexible and maintainable.

    - [__S__: Single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle)
      > A class should have only a single responsibility (i.e. changes to only one part of the software’s specification should be able to affect the specification of the class).
      <!-- -->
      > [...] The reason it is important to keep a class focused on a single concern is that it makes the class _more robust_.
      <!-- -->
      > Another way to think of SRP: Gather together things that change for the same reasons and at the same times. Separate things that change for different reasons or at different times. [A tweet by @unclebobmartin on July 29, 2018]
    - [__O__: Open/closed principle](https://en.wikipedia.org/wiki/Open/closed_principle)
      > “Software entities ... should be open for extension, but closed for modification.”
    - [__L__: Liskov substitution principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle)
      > “Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program.”
    - [__I__: Interface segregation principle](https://en.wikipedia.org/wiki/Interface_segregation_principle)
      > “Many client-specific interfaces are better than one general-purpose interface.”
    - [__D__: Dependency inversion principle](https://en.wikipedia.org/wiki/Dependency_inversion_principle)
      > One should “depend upon abstractions, [not] concretions”

- [DAMP (Descriptive And Meaningful Phrases) vs DRY (Don’t Repeat Yourself) in unit tests](https://stackoverflow.com/questions/6453235/what-does-damp-not-dry-mean-when-talking-about-unit-tests)
- [KISS (Keep It Simple, Stupid) principle](https://en.wikipedia.org/wiki/KISS_principle)
- [OAOO (Once and Only Once) principle](http://wiki.c2.com/?OnceAndOnlyOnce)
- [Principle of Least Astonishment](https://en.wikipedia.org/wiki/Principle_of_least_astonishment)
- [Principle of Least Privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege): From [TrueScript’s Variable Declarations](https://www.typescriptlang.org/docs/handbook/variable-declarations.html): “Applying the principle of least privilege, all declarations other than those you plan to modify should use `const`.”
- [YAGNI (You Aren’t Gonna Need It) principle](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it), a principle of XP

## Rules

- [The Boy Scout rule](https://deviq.com/principles/boy-scout-rule/): “Leave your code better than you found it.” You can also check [the Boy Scout rule in coding](https://skilltomastery.blogspot.com/2016/08/the-boy-scout-rule-in-coding.html), in the context of Clean Code.

## Guidelines, Best Practices, and Coding Standards

### C++

- [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines), an open source project on GitHub, led by Bjarne Stroustrup, to build modern authoritative guidelines for writing C++ code
  - Kate Gregory, _10 Core Guidelines You Need to Start Using Now_ ([talk](https://www.youtube.com/watch?v=XkDEzfpdcSg)), CppCon 2017
    1. [C.45](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rc-default): Don’t define a default constructor that only initializes data members; use in-class member initializers instead, and
      [C.48](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rc-in-class-initializer): Prefer in-class initializers to member initializers in constructors for constant initializers
    2. [F.51](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rf-default-args): Where there is a choice, prefer default arguments over overloading
    3. [C.47](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rc-order): Define and initialize member variables in the order of member declaration
    4. [I.23](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Ri-nargs): Keep the number of function arguments low
    5. [ES.50](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Res-casts-const): Don’t cast away `const`
    6. [I.11](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Ri-raw): Never transfer ownership by a raw pointer (`T*`) or reference (`T&`)
    7. [F.21](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rf-out-multi): To return multiple “out” values, prefer returning a tuple or struct
    8. [Enum.3](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Renum-class): Prefer `enum class`es over “plain” `enum`s
    9. [I.12](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Ri-nullptr): Declare a pointer that must not be null as `not_null`
    10. [ES.46](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Res-narrowing): Avoid lossy (narrowing, truncating) arithmetic conversions
  - My own incomplete list of selected guidelines:
    - On `const`ness: [ES.25](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Res-const): Declare an object `const` or `constexpr` unless you want to modify its value later on
    - On pointers: [ES.24](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Res-unique): Use a `unique_ptr<T>` to hold pointers
    - On reducing verbosity: [T.44](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Rt-deduce): Use function templates to deduce class template argument types (where feasible)
- [cppbestpractices](https://github.com/cpp-best-practices/cppbestpractices), a Collaborative Collection of C++ Best Practices, led by Jason Turner
- Herb Sutter, Andrei Alexandrescu, _C++ Coding Standards: 101 Rules, Guidelines, and Best Practices_, Addison Wesley Professional, 2004
- [LLVM Coding Standards](http://llvm.org/docs/CodingStandards.html)
- [JUCE Coding Standards](https://juce.com/coding-standards/)
- Comments:
  - _“The proper use of comments is to compensate for our failure to express ourself in code.”_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
  - _“Don’t comment bad code—rewrite it._” -- Brian W. Kernighan and P. J. Plaugher, _The Elements of Programming Style_
  - [Coding Without Comments](https://blog.codinghorror.com/coding-without-comments/) article by Jeff Atwood (from his computer programming blog _Coding Horror_)

### Python

- [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)

## Unit Testing

- _“Code, without tests, is not clean.”_ -- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_

### Frameworks

- [List of unit testing frameworks](https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks)
- Google Mock (gMock), the Google C++ mocking framework
  - :octocat: [googlemock repo](https://github.com/google/googletest/tree/master/googlemock)
  - [README.md](https://github.com/google/googletest/blob/master/googlemock/README.md)
  - [Cheat Sheet](https://google.github.io/googletest/gmock_cheat_sheet.html)
  - [Cook Book](https://google.github.io/googletest/gmock_cook_book.html)
- [GUnit](https://github.com/cpp-testing/GUnit), Google.Test/Google.Mock/Cucumber on steroids on steroids, by Kris Jusiak

#### Criticism

- Peter Sommerlad, _Mocking Frameworks considered harmful_ ([talk](https://www.youtube.com/watch?v=uhuHZXTRfH4)), CppCon 2017

### Principles+

- [Given-When-Then (GWT)](https://en.wikipedia.org/wiki/Given-When-Then),
  [Four-Phase Test](http://xunitpatterns.com/Four%20Phase%20Test.html),
  [Arrange-Act-Assert (AAA)](http://wiki.c2.com/?ArrangeActAssert)

  - From [Martin Fowler’s article](https://martinfowler.com/bliki/GivenWhenThen.html):
    > It’s an approach developed by Dan North and Chris Matts as part of BDD. [...] You can also look at it as a reformulation of the Four-Phase Test pattern.

    Four-Phase Test pattern: 1. Setup 2. Execute 3. Check 4. Teardown

    |   | GWT   | Four Ph. | AAA
    | - | :---: |:--------:| :-:
    | 1 | Given | Setup    | Arrange
    | 2 | When  | Execute  | Act
    | 3 | Then  | Check    | Assert
    | 4 |       | Teardown |

  - Example of the naming convention introduced to me by [Angel Costela](https://www.linkedin.com/in/%F0%9F%92%BB-angel-costela-sanmiguel-b84229a6/):  __Given__\_state\__A_\___When__\__B_\_happens\___Then__\_these\_conditions\_must\_be\_met\()

  - Example (written as pseudo-code):

    ```c++
    void Given_state_A_When_B_happens_Then_these_conditions_must_be_met() {
      set_state_A();                      // Given | Setup    | Arrange
      B();                                // When  | Execute  | Act
      assert(condition_1 and condition2); // Then  | Check    | Assert
      ;                                   //       | Teardown |
    }
    ```

- From _C++Now 2017_, Kris Jusiak’s “Towards Painless Testing” [(video)](https://www.youtube.com/watch?v=NVrZjT5lW5o) (published on Jun 13, 2017)

### Patterns

Some [software design patterns](https://en.wikipedia.org/wiki/Software_design_pattern):

- [Adapter](https://en.wikipedia.org/wiki/Adapter_pattern)
  > ... is a software design pattern (also known as __Wrapper__, an alternative naming shared with the Decorator pattern) that allows the interface of an existing class to be used as another interface. It is often used to make existing classes work with others without modifying their source code.

## On bugs

Since the cost of fixing a [software bug](https://en.wikipedia.org/wiki/Software_bug) soars depending on how far in the software development life cycle it is found. We should then try to locate them as sooner as possible.

Some of the most nefarious bugs we might find are [heisenbug](https://en.wikipedia.org/wiki/Heisenbug)s and those caused by code with undefined behavior.

### First and foremost: Compilers and static analyzers are our friends

#### Compilers, not compiler

#### Zero compiler warnings policy

The first tool against software bugs, perhaps right after writing clean code, and right before using static analyzers, should be using adequate compiler(s) warning flags, and achieving zero warnings. During my career I’ve suffered time and again bugs in production very hard to pinpoint that could have been eradicated simply by taking care of compiler warnings. This has a high cost in time and money, in addition to experiencing a high level of frustration.

It is important to point out that the goal is not simply “get rid of the warning” (or, in other words, “satisfy the compiler”), but to actually fix the code. In the past I’ve seen “fixes” to satisfy the compiler that actually introduced bugs--not a good tradeoff!

#### Preventive coding

Whenever possible, take advantage of __static assertions__ to discover coding problems at the compilation stage. In C++ I’m also an advocate of extensive use of the keyword `const` ([ES.25](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Res-const)), and, from C++11, forbid `NULL` favoring `nullptr` instead ([ES.47](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#Res-nullptr)).

#### Static analyzers

I’m a huge fan of [Cppcheck](https://cppcheck.sourceforge.io/), since it has helped me identifying coding bugs which could have slipped through. These coding bugs were sometimes, but _not always_, also detected by the compiler as warnings or even errors! Another helping tool you might consider using is [SonarLint](https://www.sonarsource.com/products/sonarlint/).

- [List of tools for static code analysis](https://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)

## Code Reviews

<p align="center">
  <img src="images/WTFs-per-minute-400x362.png?raw=true" alt="(c) 2008 Focus Shift/OSNews/Thom Holwerda"/><br>
  <a href="https://www.osnews.com/story/19266/wtfsm/">(c) 2008 Focus Shift/OSNews/Thom Holwerda</a>
</p>

Code reviews represent opportunities to learn and share good stuff from the [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines).

> The aim of the guidelines is to help people to use modern C++ effectively. By “modern C++” we mean C++11, C++14, and C++17.

## Incomplete list of favorite gurus

Sort of alphabetically sorted:

- Andrei Alexandrescu [@incomputable](https://twitter.com/incomputable)
- Andrew Hunt, Andy Hunt [@PragmaticAndy](https://twitter.com/PragmaticAndy)
- Andrew Sutton: :octocat: [asutton](https://github.com/asutton)
- Bjarne Stroustrup [@stroustrup](https://twitter.com/stroustrup)
- Dave Thomas [@pragdave](https://twitter.com/pragdave)
- Herb Sutter [@herbsutter](https://twitter.com/herbsutter)
- Jeff Atwood [@codinghorror](https://twitter.com/codinghorror) · [Coding Horror](https://blog.codinghorror.com) blog
- Jason Turner: [@lefticus](https://twitter.com/lefticus) :octocat: [lefticus](https://github.com/lefticus)
- Kate Gregory [@gregcons](https://twitter.com/gregcons)
- Kent Beck [@KentBeck](https://twitter.com/KentBeck)
- Krzysztof/Kris Jusiak: [@krisjusiak](https://twitter.com/krisjusiak) :octocat: [krzysztof-jusiak](https://github.com/krzysztof-jusiak), [kris.jusiak.net](http://kris.jusiak.net/)
- Martin Fowler [@martinfowler](https://twitter.com/martinfowler)
- Michael Feathers [@mfeathers](https://twitter.com/mfeathers)
- Nicolai Josuttis [@NicoJosuttis](https://twitter.com/NicoJosuttis)
- Robert C. Martin [@unclebobmartin](https://twitter.com/unclebobmartin) | [Clean Code Collection quotes](https://www.goodreads.com/work/quotes/18312943-the-robert-c-martin-clean-code-collection-collection) (from _Clean Code_ plus _Clean Coder_)
- Ron Jeffries [@RonJeffries](https://twitter.com/RonJeffries)
- Scott Meyers [aristeia.com](https://www.aristeia.com/)
- Ward Cunningham [@WardCunningham](https://twitter.com/WardCunningham)

## List of selected great books

- Andrew Hunt and David Thomas, _The Pragmatic Programmer, From Journeyman To Master_
- Martin Fowler, Kent Beck, John Brant, William Opdyke and Don Roberts, _Refactoring: Improving the Design of Existing Code_
- Robert C. Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_
  - Notes on GitHub: [jbarroso/clean-code](https://github.com/jbarroso/clean-code)
- Robert C. Martin, _Agile Software Development, Principles, Patterns, and Practices_
