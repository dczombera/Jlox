# Jlox - Implementation of the Lox language in Java

This project consists of a scanner, a parser and an interpreter for the lox language. The parser parses the source code and creates an abstract syntax tree (AST) that is executed by the interpreter. 
The lox language's syntax is a member of the C family. The language itself is dynamically typed and is pretty compact. Since the main goal of this project was to learn more about compiler and interpreter, it is by no means comprehensive.

Some of the features included are: 
- Variable binding
- Numbers
- Booleans
- Nil
- Strings
- Arithmetic expressions
- Comparison and equality
- Logical operators
- Precedence and grouping
- Control Flow
- Functions
- Closures
- Classes (including inheritance)

Thanks to Robert Nystrom and his amazing handbook [Crafting Interpreters](http://www.craftinginterpreters.com/).

## Syntax Example

```C
class Breakfast {
  init(food, drink) {
    this.food = food;
    this.drink = drink;
  }

  serve(who) {
    print "YamYam! Enjoy your " + this.food + " and " + this.drink + ", " + who + ".";
  }
}

class Brunch < Breakfast {
	init(food, drink, surprise) {
		super.init(food, drink);
		this.surprise = surprise;
	}

	surprise() {
		print "How about a " + this.surprise + "?";
	}
}

var brunch = Brunch("cheese sandwich", "coffee", "champagne");
brunch.serve("Michael");
// "YamYam! Enjoy your cheese sandwich and coffee, Michael."
brunch.surprise();
// "How about a champagne?"
```
