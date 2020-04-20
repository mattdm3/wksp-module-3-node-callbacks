# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything. 

Take the time to explain it to each other. 

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here

1 - yarn install in terminal
2 - yarn dev in terminal 

Create the server page with and set up express and server. Create endpoint for home page and app.get. Create homepage with styling that includes header and footer partials. 

create endpoint for the input query submission and trigger a handler function that adds the item to a global empty array. And the handler should send the last item of the array. 

the homepage needs to append the item of the array to the list. 

```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here

body parser handles the post request and exposes it on req.body. It creates an object out of the post method input (like in a form)


```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here

get is a user request that exposes a page and post reflects a user submission 

```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here

to make the code dry and place the handlers on another page. 

```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here

Line 1 is the empty array that will hold post request items recieved and will be updateed on each post request. 

```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here

there needs to be a response sent to the client or the browser will keep waiting 

``` 

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here

It's checking through middleware to see what the headers allow for content type. 

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here

importing the header partial. 
creates input container with the partial the input. 

content container that iterating through the items array and adding an item to the list. Each submission re-renders the whole page and re inserts the array values. 

inlcudes footer 

```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here

they are sasss variables that can be used as dynamic variables globally 

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here

It is using a sass function to calculate the content width which is a pre-set value minus 60px. 

the #{} is to interpolate variables created. 

```







