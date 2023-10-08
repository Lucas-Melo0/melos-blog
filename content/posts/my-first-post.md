---
title: "3 Things you should stop doing in JavaScript"
date: 2022-07-12T17:13:14-03:00
draft: false 
---

Today I would say that without a doubt JavaScript is one of the most popular programming languages in the world, and every time that JavaScript is talked about you hardly hear about bad practices on it so that’s gonna be the topic of today post.

## 1. Using Var
Well nowadays you should never be using “var” in your code but if you’re still using it or don’t know why you shouldn’t use you should stick around. Basically when we talk about the differences of the “old way” of declaring a variable and the new way in let and const the key is the scope of the variable.

If you’re still wondering let me clarify it for you, when you use var you’re limited to two scopes the global and the function scopes, that means that declared variables inside those scopes be it on if’s or for’s will share the same space of others variables which in big projects may cause a overwrite problem.

And there’s more because when using let or var we can limit the access of external variables which can improve the memory efficiency.

## 2. Not using strict equality ===
Honestly I would say that one of the worst things you can do while coding in JavaScript is not using strict equality, you may wonder why. Well simply putting the simple equality operator will implicitly force one of the sides of the operation making it both of them the same type.

While this may not be a problem in most cases I would recommend that for the sake of expected results always use the strict equality.

## 3. Not following proper name convention
Well which convention you may ask ? Well that depends on what are you working in and with who are you working with but that are some conventions that are accepted by a large part of the coding population such as:

Using camelCase on variables and functions names
Writting constants in UPPERCASE
Using space after commas
Those are just a few examples of many conventions that exist to improve coding readability. This is a topic that I will be talking about more in one of my nex posts that will be about a book I’m justt finished reading “Clean Code”.