# micro:bit code generator

## micro:bit "Javascript" limitations

* You cannot call a function.
* You must always use braces around `if` statements etc — in particular you cannot use `else if`. You must use `else { if ... }`
* You cannot use `switch`.
* Variables are treated as strongly typed.
* You cannot do string manipulation. (TODO: CHECK THIS)
* You cannot use arrays. (TODO: CAN YOU USE OBJECTS?)
* You cannot use increment operators, even in for loops. Use `i = i + 1`.
* You can't declare variables outside a function; put them on `globals`.
* You can't declare variables without also assigning them.
* You can't declare two variables on one line (`var a = 1, b = 2;`)

## Generator limitations:

You can call functions now, but they *must* be written exactly as so:

```
function functionName() {
	// code goes here
}
```

You cannot pass arguments to a function. You cannot make functions recursive, even in unreachable code paths, as they are inlined.

You cannot place two statements on a line if they need re-writing (eg, function calls).

## Future ideas

Using a real lexer/parser, we could:

* polyfill function arguments;
* remove syntax limitations.