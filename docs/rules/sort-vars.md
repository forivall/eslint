---
title: ESLint
layout: default
---
﻿# Variable Sorting

When declaring multiple variables within the same block, some developers prefer to sort variable names alphabetically to be able to find necessary variable easier at the later time. Others feel that it adds complexity and becomes burden to maintain.

## Rule Details

This rule checks all variable declaration blocks and verifies that all variables are sorted alphabetically. This rule is off by default.

The following patterns are considered warnings:

```js
var b, a;
```

The following patterns are considered okay and do not cause warnings:

```js
var a, b, c, d;
var _a = 10;
var _b = 20;
```

Alphabetical list is maintained starting from the first variable and excluding any that are considered warnings. So the following code will produce two warnings:

```js
var c, d, a, b;
```

But this one, will only produce one:

```js
var c, d, a, e;
```

## When not to use

This rule is a formatting preference and not following it won't negatively affect the quality of your code. If you alphabetizing variables isn't a part of your coding standards, then you can leave this rule off.
