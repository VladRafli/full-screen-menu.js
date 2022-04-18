# full-screen-menu.js

Full Screen Menu for your website navigation, usually used on website handling mobile viewport.

This library depend on TailwindCSS and animate.css CSS Class. Make sure to include it in your project too...

# How to install

For now, only available on github, so you can download the source code directly and use it in your project.

# How to use

1. Define a HTML element with id of "full-screen-menu"

```html
<div id="full-screen-menu" class="h-screen w-screen fixed top-0 bg-white md:hidden animate__animated hidden">
  <!-- Your menu goes here! -->
</div>
```

2. Then, add this script in your HTML or your custom JS

```js
// Your Button
let button = document.querySelector("#button");
// Init Full Screen Menu
new FullScreenMenu(button, 1000);
```

**Explanation**

First argument is your button element, grabbed with DOM.

Second argument is the animation duration, this is important as the menu would
suddently diminished on close if not defined.

**Customize behaviour**

You can spesify custom behaviour for the full screen menu
by calling callback on second and third parameters.

Third paramater is called when full screen menu is opened.
Fourth parameted is called when full screen menu is closed.

**Example**

```js
// Your Button
let button = document.querySelector('#button')
// Init Full Screen Menu
new FullScreenMenu(button, 1000, (menuClassList) => {
    menuClassList.add('some-class')
}, (menuClassList) => {
    menuClassList.remove('some-class')
})
```

**More than one button with same id?**

You can too..., get all your button element by same id.
then pass it to the class

```js
// Your Button
let button = document.querySelectorAll('#button')
// Init Full Screen Menu
new FullScreenMenu(button, 1000)
```

# License

MIT