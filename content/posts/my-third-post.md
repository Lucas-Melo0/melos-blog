---
title: "3 React tips you should know to become a better engineer"
date: 2022-09-17T17:13:14-03:00
draft: false 
---
When learning React its normal to focus on the more pressing topics like components and rendering those components so its not unusual that when pushing something for production you might set aside somethings that at the time you felt that were not so important for your application. That being said in this article I’m gonna talk about three React “Hidden” tips and when you should use them.

1. Key prop
I’m sure that at some point in time when you we’re building an app and opened your console you received the warning below

Warning: Each child in a list should have a unique key prop.
And thought to yourself “Damn I forgot to pass the map index as a key” and I’m here to tell you why you shouldn’t be doing this.

Well for starters this is what React already does by default, so when you pass the index as a key you’re really not doing anything you’re just shutting off the warning but the problem remains.

And the problem is that React has a hard time keeping track of elements between updates so that’s why you should pass a unique key when rendering from an array of items like an id that comes from your backend.

To illustrate this problem you can click on the fruits at this [demonstration](https://react-fundamentals.netlify.app/isolated/final/07.extra-1.js) by the amazing Kent C. Dodds.

2. Lazy initializing

When using React built-in Hook useState is quite common that we pass an initial value to it but in some cases this initial value can be computationally expensive like getting a value from localStorage for example

And we might just need this value one time so to keep doing this computationally expensive operation every re-render is a big nono.

So in this case we turn the localStorage access into a function and pass its declaration as the initial value of useState and then this function will only be called on the first render of the component.

This will be called at every re-render.

```React
 const [value, setValue] = useState(localStorage.getItem("key")) 
```

This will only be called at the first render.

```React

const keyGetter = () => localStorage.getItem("key") 
const [value, setValue] = useState(keyGetter)

```
3. React Dev tools

The third tip its not in react per se but if you use correctly it will drastically improve your coding experience.

React Dev tools is a great chrome extension that makes way easier to analyze your React application you can get details like props,hooks,state,components and see the reason behind a component render so it makes debugging more efficient.


That’s all for today folks, Thank you so much for reading it, and I just want to make it clear that in spite of the title there is no tip in the world that will make you into a better engineer overnight, this might seem obvious but if you don’t understand something that you’re doing stop and study it because knowledge also has a compound effect to it and it’s dividends are huge.