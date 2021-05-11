# Clean-Code

# Video #2 | [5 Tips for Cleaner Code](https://www.youtube.com/watch?v=tBigGpLRMtU)


1. Delete/remove out the big blocks of comments, or have them in a version control.
2. Delete old comments as you refactor the code base.
3. Avoid comments and write good functional tests.
4. Follow D.R.Y principle (Don't repeat yourself): Repeating something over and over again is a **code smell**. If the code/logic is repeating put in a function/method, library or service etc. Learn to write LESS!
5. Naming Conventions: Follow style guide from company or framework/library. 
   - Linters might catch this.
6. Make readable code.
    - Don't use special one liners or tricks.
    - Readable code is more maintainable
    - Think of next person who will have to deal with your code.

7. Test your code: Manually test it! Better to write End-to-End (E2E) or unit test, depending upon the requirements. Make sure you do a minimal automated test.
8. Keep Function Small: The single responsibility principle (**SRP**) is a computer-programming principle that states that every module, class or function in a computer program should have responsibility over a single part of that program's functionality, which it should encapsulate.

<hr>

# Video #3 | [The Art of Clean Code by Victor Rentea](https://www.youtube.com/watch?v=AeWbJ5LIFNg)

> Anyone can write code that a computer can understand, but few programmers know how to write **code that a human can understand**.
>
> -- <cite>Martin Fowler</cite>
>
> <small><i>author of **Refactoring**</i></small>

## 1. Why Clean Code?

- True cost of software = its maintenance
- We **READ 10x more** time than we **WRITE**. Make it more readable, even if it's harder to write.
- Boy scout rule: Always check in cleaner code than you found. Whenever you are changing anything in the code base, make an effort to leave the code in a better place in terms of readbility than when you found it.
- The day you stop refactoring, the day it becomes legacy.

## 2. Naming:
   1. Avoid abbreviations, unless it's a basic business concept, like VAT.
   2. Continuous Renaming: There are no perfect names, rename as you learn the application. (Team and you will be **grateful** in 3 months, LOL)
   3. Consistent: find(), fetch() or get(), stick to naming conventions.
   4. Unique: Synonyms confuse, Don't use buyer or clientto refer a customer. Don't leave any ambiguity.
- Functions are verbs:
  -  ~~product()~~ : **search**Product()
  -   ~~transaction()~~ : **send**Transaction()
  - Make the name speak for iteself instead going over the comments, implementation or documentation. Rename the function when you found a better name. **Comprehension Refactoring** by Martin Fowler.
- Boolean name should answer yes/no:
  - <u>is</u>GoldClient()
  - <u>are</u>HostsValid()
- Classes are nouns
  - Customer, OrderDetails, OrderFacade
- Avoid meaningless names
  - Order~~Info~~, Order~~Data~~ vs Order

## 3. Functions:
A function **should do one thing**, it should do it well, and it should do it ONLY.
- Function should be SMALL: 5 lines, **LOL**! Should not take your your entire screen and if it takes too much time to understand, BREAK IT DOWN!
- Performance? Smaller methods run faster. **Just-In-Time**-Compiler Optimizations. Break it down into samller function with good naming if you can't remember which goes where as number grows but the TEAM will be **grateful** in 3 months.

> Premature optimization is root of all evil.
>
> -- <cite>Donald Knuth</cite>

- Avoid returning null, instead use optional (?) or Throw exception.

- Global exception handler. Avoid writing `catch` in business logic code. Minimize as much as possible.
- You are not donw when the code starts working. You need have have a **Coninuous Refactoring** approach. Reflect on the code and better ways to design.
- As soon as code starts working, cleanup your code and build your own design skills.
- Early return makes the code less nested and complex.

## 4. IDE
- Learn IDE shortcuts. When you will have to do a major restructing you have to move lightning fast.
- A line shouldn't be more than 120 chars, EVER!
- Function: 5-10 lines and less than entire screen height.
- Class should be 100-200 lines and never more than 500.

## 5. Comments

### Bad Comments

- Comments = Failure, Comments are written expression of your incompetence? NANI!? 
- Come back and refactor, improve the expressiveness of the code. 
- Comments inevitably fall out of sync with the code.

### Good Comments
- Specific Algorithms
- Bug Workarounds
- Explain call to a strange API
- Warning of consequences
- TODO: // TODO Good morning
- For libraries/frameworks you write

<hr>

# Video #4 | [How to Write Clean Code Even a Baby Can Understand](https://www.youtube.com/watch?v=Tb2ufLHy65k)

- Don't write 💩 PUPU code! :D
- Take time, don't rush, be professional.
- Use meaningful names.
- Make use of variables to make it super readable irrespective of number of lines.
- One line of code per thought.
- Avoid pesky comments: If you need comments all over the place, you are doing something wrong.
- Comments are lies waiting to happen: Code doesn't match the comment as refactoring takes place.
- Make use of Single Responsibility Principle (SRP).

<hr>

# Video #5 | [Tips for cleaner code: Cleaning up IF statements](https://www.youtube.com/watch?v=ldqDpmMkXgw)

- Always return what you are expecting last.
- Do the checks that you need first and don't nest any return values you expect to see. Early return.
- Check in negative and return early. Multiple if, but not nested.

<hr>

# Video #6 | [3 More Tips To Write Clean Code](https://www.youtube.com/watch?v=OHQoytCkQUY)

1. More Identation/nesting = Less readability
2. Consistency: In variables names, files names, folder strcuture in the entire codebase.
3. Variable names should be consistent within the same function. `removeBtn` , `addButton` - not consistent.
4. If you use `async` & `await`, use it for entire codebase, and avoid `then` and `catch` or vice-versa.
5. Write your code which is self explanatory that doesn't need commenting.
6. Document/Comment the code which is not self explanatory.

# Video #7 | [Write BETTER Code! 7 Tips to Improve Your Programming Skills](https://www.youtube.com/watch?v=vfqvzgkYYF0)

1. Avoid Abbreviating variables. Only use abbreviations which are universally recognised. Example: URL, VAT etc.
2. Limit function arguments. And use destructing inside or put them in an object before passing into another.
3. Simplify Conditional Expressions
4. Declare Variables close to their usage: Declaring variable at the top and using it way below is difficult to debug.
5. Avoid unintended consequences in functions: Name of the function should tell what the function is doing. Don't add any other things which can't be explained by the function name.
6. Function should do one things only and do it well(Avoid long function)
7. Zombie code: The code/feature/commented code block that you wrote and thought will come back to it later proves to cause unintended consequence if left unattended. Never put this into production. Use git/version control properly for such cases.

# Video 8 | [SOLID Principles | Code Like a Pro](https://www.youtube.com/watch?v=ppoKxa60jhI)

- **S**: Single Responsibility Principle
  - A class should have one, and only one, reason to change.
- **O**: Open Closed Principle
  - You should be able to extend a classes behaviour, without modifying it. Adding features without modifying the previous code.
- **L**: Liskov Substitution Principle
  - Derived classes must be substitutable for their base classes.
- **I**: Interface Segregation Principle
  - Clients should not be forced to depend on methods that they do not use.
- **D**: Dependency Inversion Principle
  - High level modules should not depend upon low level modules. Both should depend upon abstractions.

By Robert C.Martin: Uncle Bob

# Video #9 | [Clean Code: Formatting and Comments](https://www.youtube.com/watch?v=HzWf-EeE3uI)

### Formatting
- Its subjective.
- Not to argue over formatting, chose a certain type of formatting between you and your team.
- Use consistent capitalization.
- Function callers and callees should be close.

### Comments
- Only comment things that have business logic complexity
- Don't leave commented out code in your codebase.
- Don't have journal comments: That's what `git log` is for.
- Avoid positional markers: Fancy design where what is.

# Video #10 | [The Art of Code Comments - Sarah Drasner](https://www.youtube.com/watch?v=yhF7OmuIILc)

> The comments are an excuse for not writing the code better to begin with.

There is no one true way of writing comments. There is no YES comments or NO comments, it thoughtful comments that are good for the maintainer to read.


### Good Comments

- Code can describe **HOW**, but it cannot explain **WHY**.

- Clarify what's not typically legible by humans.

- A larger piece of code that has to exist, sometimes commenting different sections or making some separation can help people find their way more quickly.

- A guide to keep the logic straight while writing the code is OK, like a todo list for implementing logic but shouldn't be kept around once done.

- Commenting as a teaching tool.

- Add reference links to the site that you copy pasted code from, it could helpful later since someone might answer with a better a solution.

### Bad Comments

- They just say what it's already doing.

- Comment is literally part of the code, and has to convey what the code below is doing. Needs maintenence as refactoring takes place. Often ends up being misleading if not maintained.

- Refactored code should be in version control which could be retrived and should not be commented out in codebase.

- Could have used a better name if you are commenting to tell what the name means.

- We spend time writing the comment that could be better spent making the code a little cleaner to begin with.

# Video #11 | [Writing Readable Code](https://www.youtube.com/watch?v=SPlS4kW0UbE)

- Have and follow a style guide.
- Limit line length (80 characters)
- Bunch of parameters, split them up, one for each line.
- Long lines are hard to read.
- Write code that doesn't need comments.
- Make the code more obvious by assigning it to a function expression with a proper name or to a variable.
- Comments -> Logging
  
- Naming: `getData()` while fetching from a external source is not a good naming convention. Instead use `fetchData()`. `getData` is a simple method like an accessor that doesn't take long. So wrong naming convention. So computatinally extensive process could be name as `generateToken` or `createToken`.
- Extra 5-10 mins spent on coming up with a better name will go a long way. Decrease technical debt and maintenence.

> All code in any code-base should look like a single person typed it, no matter how many people contributed.
>
> -- <cite>idiomatic.js</cite>

- When you have a variable or function that it returns a boolean, make crystal clear that this value or functions holds boolean. It can be only `true` or `false`, no side-effects.
  - Use prefix like: `shouldShowOneDeiveImport`, `isEmpty`, `canCreateDocuments`, `hasLicense` etc

- Boolean Trap: 
  
  ```javascript
  page.getSVG(dpi, true, false)
  ``` 
  boolean parameters.
- Deobfuscate Boolean Parameters. Use a object when a method takes 4 arguments.
  ```javascript
  page.getSVG({
    imageDpi: dpi,
    includePageBackground: true,
    compress: false
  })
  ```
- Or annotate a line for each if you don't want to use an object or it isn't feasible.

  ```javascript
  page.getSVG({
    /* imageDpi */ dpi,
    /* includePageBackground */ true,
    /* compress */ false
  })
  ```

- Its all about readability.
- Practicing readability
  - Code reviews: ask for feedback: drop a comment and ask for a better name.
  - Code reviews: give feedback
  - exercism.io

# Video #12 | [Writing Clean Code - Intention-Revealing Names](https://www.youtube.com/watch?v=tePvLAefzmQ)

- Always use descriptive, intention revealing names when creating a variable, function, classes, objects etc.
- Not a good idea to use numbers in a variable.

# Video #13 | [Code Like a Pro : Functions | How to Write Code Professionally (With Examples)](https://www.youtube.com/watch?v=bF9yP9rI_Bs)

Readable, Searchable, Understandable code = Maintainable Code.

- If a function is more than 10 lines long, consider refactoring.
- Functions and methods are verb and we need to treat them as such.
- Long variable names are descriptive variable names.
- Eliminate global variable using a function and get the data using by returning and assigning to a variable.

```javascript
const getValues = (): <any[]> {
  const calc = ...
  const done = ...
  const edit = ...
  return [calc, done, edit]
}

const doSomething = () : void => {
  const [calculations, doneWork, editText] = getValues()
}
```

- Take functional approach and eliminate side effects.

- Confused instructor. :<

# Quick bits

- YAGNI: You Aren't Gonna Need It is a principle of extreme programmer's shouldn't add functionality until it's deemed necessary.

- KISS: Keep It Simple, Stupid as a design principle states that most systems work best if they are kept simple rather than made complicated. Therefore, simplicity should be a key goal in design, and that unnecessary complexity should be avoided. 

# Video #15 | [Simplicity: Not Just For Beginners (or How To Write Simpler Code)](https://www.youtube.com/watch?v=W2Thd9nKqmU)

### What is simple code?
- Expressive
- Readable
- Understandable
- Unsurprising
- Transparent
- Self explanatory
- Reassuring
- Pleasant

## Is it faster/correct to write simpler code?

- No, it requires new habits, new ways of looking and most importantly: reviewing, revisiting, refactoring.
- Simpler code is more readable, debuggable and often more correct too.
- Staying consistent is the way to maintainable code.
- Code that moves complexity to abstractions often has less bugs.
- Library code is already tested and has thought of edge cases.
- To get faster code you typically have to know and remember something about the language.
- Try not to chose simplicity over performance **if** a real choice exists: Build then optimize.
- Library code may be faster than what you would write yourself.
- Unsurprising code is more maintainable code.
- Expressive code is fun to work with.
- Other people's code is **B-E-A-U-T-I-F-U-L**, embrace it! :D
- True simplicity is very hard. You have do know in-and-out's of a programming language.

### Steps:
1. Getting a understanding of what simple code looks like.
2. Try to code simply from the beginning.
3. As it grows and when it becomes too complex, make it simpler.
4. Maintain consistency.
5. Good names really helps: avoid single character variable names.
6. Short function with a proper name to hold a loop (since loops don't have names).
7. Avoid really long list of parameters.
8. If a function needs 10 parameters, then maybe it requires more than, maybe 3 functions that could be called with smaller parameter lists.
9. Don't nest deeply - return early.
10. Mark everything const that you possibly can. Having to keep track of more local variables that don't vary increases cognitive burden.
11. Keep up with the standard/libraries.

  > Programming is a social activity in which communication is a vital skill. The code you leave behind speaks.

### Simplicity Paradox:

1. The things you do to make code simpler can make it more complex.
2. It is NOT POSSIBLE to write simple rules for how to write simple code.

### Replace your complicated things with 
- familiar idioms and language constructs.
- Well known library classes and functions that **others will recognize**.
- Appropriate abstraction that becomes **a thing to learn** in you code, moving complexity inside your abstraction.

---

# Video #16 | [Peter Hilton - How to write maintainable code](https://www.youtube.com/watch?v=6jmUmZX2pok)

- Use a consistent coding style.
- Keep up with new things and embrace it.
- Good names for everything are the key to clean code but its hard. Use software tools (word games, thesaurus), practice, git gud!
- Naming smells: be descriptive. 
  - No abbreviations unless globally accepted. 
  - Numeric suffixes. 
  - Abstract names like `data`, `object`.
  - Vague words: `getPrice`

### How to name things:
- Learn to recognize bad naming
- Refactor - rename bad names to better names
- Improve your vocabulary by reading or gaming.
- Wield your thesaurus and dictionary.
- Adopt better naming practices
- Learn to write.

- WRITE EXPLANATORY FUNCTIONAL TESTS

### Write good comments

Comments are part of the code, so maintain them!

1. Try to write good code first
2. Try to write a one-sentence comment
3. Refactor the code(make it easier to explain)
4. Delete unnecessary comments
5. Rewrite bad comments (all good writing requires re-writing)
6. Add detail where needed(which isn't often)

DRY
### The Rule of Three

When you see duplication once, let it be because its hard to tell from just 2 occurances what the abstraction is. If you see the same things 3 times, then you refactor.

- Apply **The Rule of Three** before you remove duplication.

### Constantly improve the code

Take the **Boy Scout Principle** seriously (actually enforce it)
- Do code review on all changes
- Recognize code smells
- Refactor

Accept that maintainable code costs more.Even if you can't win, you can lose more slowly.
- Keep codebase small
- Increase refactoring effort as it grows

### Write a project introduction
Write the minimum viable system documentation.
README file in Github repo!

- Explain the system's purpose (What is the business reason? Why are we here?)
- Describe the scope (What defines what the system does and doesn't do?)
- Summarise what it does (What does it actually do? What is it for?)

---

# Video #17 | [GOTO 2016 • Seven Secrets of Maintainable Codebases](https://www.youtube.com/watch?v=0oDporwhToQ)

[Good Video!]

- Focus on the code that really matters. Most of the files in a codebase are rarely needs maintenance over longer period of time.
- When it comes to maintainable codebases, complexity isn't the problem atleast not on its own. We can't discard complexity entirely. We just to find when it matters and when it not.
- Data Analysis of codebase: Github.

---

# Video #18 | [JavaScript Best Practices and Coding Conventions](https://www.youtube.com/watch?v=RMN_bkZ1KM0)

1. Magic Number: Assigning a number with no clear meaning, example in a loop condition expression, replace it with a name constant.

  ```js
  const SECONDS_IN_A_DAY = 86400

  for (let i = 0; i < SECONDS_IN_A_DAY; i++) {
    // ...
  }
  ```
2. Avoid deep nesting and instead use methods to return the same

3. Stop writing comments, try to make code self-documenting. Code must speak for itself.

4. Avoid large functions. One thing a time.

5. Code repetition. Parameter destructing etc
6. Variable Names, `camelCase` and use meaningful name. `data` is vague so be descriptive.
7. Favor descriptive over concise.
8. Use consistent verbs per concept.

```js
getQuestions; // get
returnUsers // get
retrieveUsers // get
```

9. Make booleans that read well in if-then statements. Ex: add prefixes like is, are, has, should, can etc

10. Use nouns not verbs for classNames. They are something, they don't create something.

11. Use PascalCase for className.

12. Capitalize constant values. SNAKE_UPPERCASE

13. Avoid one-letter variable names, can be used as index in small loops or small functions.

# Video #19 | [Code Refactoring](https://www.youtube.com/watch?v=vhYK3pDUijk)

### What is Refactoring?
- Refactoring makes code understandable and easy to extend.
- Refactoring makes it quicker to create complicated systems or add new features without introducing bugs.
- Should not change the program in any tangible way
- Re-writing code is not refactoring.
- Refactoring itself doesn't directly benefit you. Instead it benefits you by enabling you to do more.
- Refactoring is most commonly done as part of the maintenance/updating step.

### Why should one Refactor?
- Remove excess code so it is easier to understand & modify
- Helps you understand others code
- Eliminate the need to remember what old code does
- Can write code quicker, add features quicker.

### What is Bad Smells?
- Duplicated Code
- Long Methods (5-10 lines)
- Complex Conditional Statements
- Primitive Obsession: Using primitives over class objects
- Indecent Exposure: Access modifiers, private classes
- Solution Sprawl: Solution that is being used across multiple classes instead having them in one place
- Alternative Classes with different interfaces
- Lazy Classes: Don't do much on their own and their capabilities should be moved to a class
- Large Classes: Too many responsibility, too many lazy class
- Switch Statements
- Combinatorial Explosions: Many methods that could be done in one method
- Oddball Solutions: Solve the problem in may different ways, select the best and remove the duplicates.


# Video #20 | [Code Refactoring - Return Fast](https://www.youtube.com/watch?v=lpB7PLSikw8)

Fail Fast: If you have an error you should fail quickly, you shouldn't propagate this error into the program.

Exit Point: Exit points a function should have. Don't really care but there are some who cares about it being only one.

Returning Fast
