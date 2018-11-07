# How to Leverage JavaScript Events

## Learning Goals

* Define a JavaScript event
* Identify different types of user events
* What are JavaScript events?

## Introduction

We've experimented with selecting and manipulate nodes in the DOM using
JavaScript. We've also experimented with creating and removing elements.
Wouldn't it be more interesting if we made those types of thing happen
when we did something--such as clicked on an element, pushed a button,
or moved our mouse? Those actions are called "events." In JavaScript we
can "listen" for events and use them to call functions that update the
DOM. In this lesson, we'll learn how to do just that.

## Define a JavaScript Event

JavaScript has event handlers that respond to user actions--user actions
such as mouse clicks, key presses, or window resizing. We can define code
that will be run when those events happen.

JavaScript allows us to bind - or connect - functions to particular events.
We create a function, and then tell the browser to run that function whenever
that event happens.

## Identify Different Types of User Events

Javascript gives us a few different event handlers that can be used.

### Mouse Click

Lets pretend we wanted to do something every time the user clicked on an image.

Should our examples look like this?
```js
    let image = document.querySelector("#kitten")

image.onclick = toggleClass;

function toggleClass(){
  if(image.className == 'image'){
      image.className = ''
  } else {
      image.className = 'image'
  }
}
```


### Key Press

Click events make up the majority of events listened you'll use, but other
events you might use include `keypress`, `keydown`, and `keyup` events will
have a `which` property that tells us which key was pressed. Try it out by
copying and pasting the following in your js console in the browser:

```js
const input = document.querySelector('input')
input.addEventListener('keydown', e => console.log(e.which))
```

### Form Submission

HTML page usually uses a submit button to submit a form to a handling file
such as a php script. All input values of the form will be transferred to
the handling file by `post` method. To submit a form to the server manually,
we can call `form.submit()`.

```js
let form = document.createElement('form');
form.action = 'https://google.com/search';
form.method = 'GET';

form.innerHTML = '<input name="q" value="test">';

// the form must be in the document to submit it
document.body.append(form);

form.submit();
```

## What are JavaScript Events?

It is important to note that web events are not part of the core JavaScript
language — they are defined as part of the JavaScript APIs built into the browser.
This means that different browsers can often support different sets of events, or
have different names for them.

Another thing worth mentioning is that events are not particular to JavaScript.
Most programming languages have some kind of event model which will often differ
from JavaScript. Even JavaScript for web is different from JavaScript in other
environments.

For example, Node.js enables developers to use JavaScript to build network and
server-side applications. It doesn't sound different, but the code _is_ quite
different. You can also use JavaScript to build cross-browser add-ons with
WebExtensions.

You don't need to understand other environments just yet, but these are some
examples that illustrate that JavaScript can vary.

## Conclusion

JavaScript allows us to do amazingly complex stuff with a simple function call.
Now that you have been given the basics of events to get started, you can explore
more event handlers! [Here's a list](http://help.dottoro.com/larrqqck.php) of a
ton of browser events.

Some other common events are are 'scroll', 'mouseenter' and 'mouseleave', 'focus',
'blur',  and 'onchange'. There are lots and lots of events - what events do popular
websites handle? This might feel intimidating at first, but it's
important to familiarize yourself with it so you can get the hang of it!

## Resources

- [MDN - Web Events][MDN]
- [StackOverflow - Bubbling and Capturing][SO]
- [QuirksMode - Event order][QM]

[instructions]: http://help.learn.co/workflow-tips/github/how-to-manually-open-a-lab
[help-center]: http://help.learn.co/the-learn-ide/common-ide-questions/viewing-html-pages-in-the-learn-ide
[MDN]: https://developer.mozilla.org/en-US/docs/Web/Events
[SO]: http://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing
[QM]: http://www.quirksmode.org/js/events_order.html