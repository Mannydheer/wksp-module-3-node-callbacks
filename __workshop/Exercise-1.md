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
// inclass notes



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
the .use will load the middleware function. 
.use body parser will allow you to use bodyParser();
Both these .use are needed for PUT and POST requests.
Sending data in the form of objects and then asking the server to store the data(object) which is in the req.body... of the PUT POST request. 

- express.bodyparser is most probably to recognize the incoming request as JSON object. 
- express.urlencoded() is a method inbuilt in express to recognize the incoming Request Object as strings or arrays.
```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here
When you are requiring this file, /handlers, you are requiring all the functions within the file..

```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

Items is an empty array where data from the handleFormData function will be pushed. In handleFormData, each item of the body will be stored into item object. Then each will be pushed into the array items.


```
// Answer here

```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here
Bebcause you want to update the homepage with the new body data that is inserted?


``` 

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here
There needs to be more specificity now to cover all the different types of data that can be requested. 

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here
in TODOinput, we are creating a form tag which will show most of the heading area of the page. The input where we can type data will be shown. The submite button. The key here is that, once it leaves this form tag, or does everything in it, it will proceed with the action to the endooint /form-data which will trigger the corresponding function. This function handleFormdata will now GRAB the data inputted and store it in item witht he use of req.body.item. Next it will push in the array items all that data inputted and trigger the homepage get point which will call handleHomePgae function. 
<!-- - -->
in HOMEPAGE, this function of handleHomepgae will now render the homepage function and pass it all the data of items as items. Next if we go on the homepage.ejs, a forEach function is run for the items array with all the data, and through the foreach, each item will actually be displayed for the user to see. 




```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here
These are variables that are declared which can be availabel for reuse instead of constantly retyping the kind of styling we want. We can simply now just call the variable and insert it in our css. 

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here
In this case we can embed the result of the sass expression - contentwidth into CSS. 
Also known as interpolations, similar to string concatenation, but you can but any variable within this #{}, if any type. 
https://sass-lang.com/documentation/interpolation
https://webdesign.tutsplus.com/tutorials/all-you-ever-need-to-know-about-sass-interpolation--cms-21375
- Once you declare vairables in SASS, you can insert them into #{} and it will give the value of the variable. 
- This allows you to reuse certain variable values inside your SASS styling which will then be generated as the original values on the CSS document. 
//Excellent youtube video for understanding. 
https://www.youtube.com/watch?v=b86xesxuQIg

```







