# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything. 

Take the time to explain it to each other. 

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here

Set up header and footer partials ejs. 
Also the form partial which has all the inputs
Code in the server so that whatever in inputted will be displayed through javascript. 


```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here
- The bodyParser module is first required in the server. The bodyParser allows to retreive data that was injected into the body of the document through body.req. Through HTTPrequests, we are POST or PUT data and then we can access this data through body.req. 
When we are on a login page, we are asking user for an email and password, then we can access this through req.body. 
In this case, whatever the user inputs, we go get it with req.body and then store it into item. Then with item we do the rest...

```
BODY PARSER LINKS
https://alligator.io/nodejs/req-object-in-expressjs/
https://stackoverflow.com/questions/38306569/what-does-body-parser-do-with-express
## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here

```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here

```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here

```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here

``` 

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here

```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here

```







