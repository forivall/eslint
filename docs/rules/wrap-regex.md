---
title: ESLint
layout: default
---
# Require Regex Literals to be Wrapped

When a regular expression is used in certain situation, it can end up looking like a divison operator. For example:

```js
function a() { 
    return /foo/.test("bar");
}
```

## Rule Details

This is used to disambuguate the slash operator and facilitates in more readable code.

The following patterns are considered warnings:

```js
function a() {
    return /foo/.test("bar"); 
}
```

The following patterns adhere to this rule:

```js
function a() {
    return (/foo/).test("bar");
}
```
