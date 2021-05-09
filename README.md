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

# Video #10 [The Art of Code Comments - Sarah Drasner](https://www.youtube.com/watch?v=yhF7OmuIILc)

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

# Video 11 | [Writing Readable Code](https://www.youtube.com/watch?v=SPlS4kW0UbE)