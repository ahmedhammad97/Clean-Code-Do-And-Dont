# Clean Code Do And Don't
Some of the software books tend to guide us through some rules and tips about how to write software code, the problem is that it is usually hard to recall the tip when you actually need it -at least I do. So I thought of doing a Do/Don't list of these rules and tips, to be easy for me to recall.

These tips are mainly my reading notes following [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.goodreads.com/book/show/3735293-clean-code)
by Robert C. Martin, and some parts of [Refactoring: Improving the Design of Existing Code](https://www.goodreads.com/book/show/44936.Refactoring) by Martin Fowler and Kent Beck, alongside with a few blog posts.

#### Disclaimer:
These tips do not cover all the materials mentioned above, it is my *opinionated* selected notes that I *personally* think it fits my every-day practices. Some important tips are left out for example just because I know them by heart. If you are looking for a full summary, check [jbarroso/clean-code](https://github.com/jbarroso/clean-code).

With that said, I will be so glad if anybody finds this to be helpful.

--------------

#### "Clean code is code that is written with care. It is simple, elegant, and efficient."

- Use intention revealing names
- Avoid misinformative names
- Use searchable names
- Name classes using *nouns*
- Name methods using *verbs*
- Be consistent with naming
- Use domain names
- Avoid unnecessary prefixes or postfixes
- Name similar variables in different levels of abstraction by different names

<br />

- Write small functions (ideally less than 20 lines)
- Minimize indentation level inside a function (ideally less than 3)
- Remove dead (unused) functions (version control is keeping it don't worry)
- Keep configurable data at high level (away from the core code)
- Write non-sectioned functions (does only one thing, not even side effects)
- Put functions with the same level of abstraction together
- Sort functions by level of abstraction
- Bury switch statements into low-level modules with Abstract Factory and Polymorphism
- Use static functions only when it is not owned by any object
- Minimize the number of arguments to a function
- Avoid boolean arguments (split it to two functions instead)
- Wrap multiple arguments into one object if possible
- Encapsulate multiple conditions into one check function
- Avoid side effects inside functions (wrap both in a parent function instead)
- Avoid output arguments (let the output object change itself)

<br />

- Write clear code (refactor) instead of adding comments
- Avoid inaccurate comments
- Remove commented-out code
- Never use redundant comments

<br />

- Avoid long code lines (ideally less than 85 chars)
- Enforce a pre-agreed coding style to all the team
- Always follow standard conventions

<br />

- Use objects when you need to hide data and expose functions
- Use data structures when you need to expose data
- Use procedural code when you need a lot of functions, few data structures
- Use object oriented code when you need a lot of data structures, few functions

<br />

- Throw exceptions rather than returning `False` or `NULL`
- Write informative error messages

<br />

- Write unit tests that covers every bit in the production code
- Write clean, neat, and "easy to evolve" tests
- Write fast, independent, repeatable, and self-validating tests 
- Test a single concept for every test function

<br />

- Design small classes
- Use single responsibility per class
- Never allow base classes to depend on their derivatives
- Isolate code entities from each other by limiting what each knows about the others

<br />

- Separate startup processes (ex. object constructions) from run-time logic
- Avoid "lazy initialization" unless used by dependency injection
- Use domain specific language suitable for the system
- Move object creation responsibility to a dedicated object (ex. DI)
- Make sure your design:
   - Run all test
   - Contains no duplication
   - Express the intent of the programmer
   - Minimize the number of classes and functions

<br />

- Use concurrency code only when there is a lot of waiting time
- Separate (Plug away) concurrency code from other code
- Avoid threads collision by avoiding shared data in the first place if possible
- Avoid using concurrency when you cannot afford major changes in design
- Use only one method on a shared object
- Keep synchronized sections small
- Never run a concurrent code out of a container
- Avoid using hard-coded concurrency commands (`sleep`, `wait`, etc.)

<br />

- Consider using duplication at early development stages ([WTF why?](https://overreacted.io/goodbye-clean-code/)), refactor later

**End**

Any further contribution is welcomed.
