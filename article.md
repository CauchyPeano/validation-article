# Using Validation in Vavr

or 

# Validation in Java: your next friend after java.util.Optional (?)

Vavr is simple yet powerful library intended to make your life better and also importantly make your code better!

There are seemingly simple classes which could make great positive impact to your application. One of them is Validation class, which I want to explain in this article.

Validation class in not invention of vavr library, idea of it came long time ago. One of the foundational concept of Validation is Applicative Functor introduced in many functional languages.

** Funny pic: whaaat, again this stuff about monads, applicative functors, etc? **

Ok, ok! Fear not dear reader, I will try my best to not use those mystical words (but if you know them it's really cool). 

## Problem

Some time ago I've got fairly simple task to parse some old banking format. This format was looking like usual csv file with only difference that it had different type of records prefixed with different 
type descriptors.

It was looking something like this:

```
REC,00001,30,100.00
REC,12345,31,20.00
TOTAL,2,120.00 
```

Usually such problem is solved via simple parsing and communicating parsing errors as exceptions:

```java

try {
	ParsedFile result = parseFile(content);
} catch (ParsingException ex) {
	ParsingError err = ex.getError();
	// handle error or write it to log
}

public ParsedFile parseFile(String content) {
	
}

```


## Validation combine

(example from Vavr)


## Controlling flow direction

### Short-circtuiting

(example when failing on first error)


### Aggregating

(example when failing with all errors)


## Validation parsers! 



