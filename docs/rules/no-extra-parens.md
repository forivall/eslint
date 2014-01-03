---
title: ESLint
layout: default
---
# Disallow Extra Parens

This rule restricts the use of parentheses to only where they are necessary.

## Rule Details

The following patterns are considered warnings:

```js
a = (b * c)
```

```js
(a * b) + c
```

```js
typeof (a)
```

The following patterns are not considered warnings:

```js
(0).toString()
```

```js
(function(){}())
```

## Further Reading

* [MDN: Operator Precedence](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
