---
layout: cover
download: https://antfu.me/talks/2021-04-29
highlighter: shiki`
title: DOM & Event Handling in JS
coverAuthor: Subramanya Rao
titleTemplate: '%s - Subramanya Rao'
hideInToc: true
info: |
 <h2>DOM Manipulation & Event Handling</h2>
  <a href="https://gdsc.community.dev/rns-institute-of-technology-bengaluru/" target="_blank" rel="noreferrer"><img alt="GDSC Logo" class="w-48px" src="https://res.cloudinary.com/startup-grind/image/upload/c_fill,dpr_2.0,f_auto,g_center,h_1080,q_100,w_1080/v1/gcs/platform-data-dsc/events/logo_QTdLJEf.jpg"></a>

  [Subramanya Rao](https://github.com/Subramanyarao11) at [GDSC RNSIT](https://gdsc.community.dev/rns-institute-of-technology-bengaluru/)

  - [Source code](https://github.com/antfu/talks/tree/master/2021-04-29)
  - [Slides](https://antfu.me/talks/2021-04-29)
---

# DOM Manipulation and Event Handling

Introduction to DOM Manipulation and Event Handling in Javascript

<div class="uppercase text-sm tracking-widest">
Subramanya Rao
</div>

<div class="abs-bl mx-14 my-12 flex">
  <img src="https://res.cloudinary.com/startup-grind/image/upload/c_fill,dpr_2.0,f_auto,g_center,h_1080,q_100,w_1080/v1/gcs/platform-data-dsc/events/logo_QTdLJEf.jpg" class="h-8 mt-2">
  <div class="ml-3 flex flex-col text-left">
    <div><b>Web Development</b> Workshop @ GDSC, RNSIT</div>
    <div class="text-sm opacity-50">Jan. 13th, 2024</div>
  </div>
</div>

<div class="abs-br mx-14 my-12 flex gap-6">
  <a href="https://github.com/webup/openfunction-talks/tree/main/202-node-async" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
  <a href="https://github.com/webup/openfunction-talks/raw/main/202-node-async/202-node-async.pdf" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-download />
  </a>
</div>


---
hideInToc: true
layout: intro
---

# Subramanya Rao

<div class="leading-8 opacity-80">
Core team member of GDSC RNSIT<br>
Full Stack Developer at WeFrameTech<br>
A fanatical Javascript Developer<br>
</div>

<div class="my-10 grid grid-cols-[40px,1fr] w-min gap-y-4">
  <ri-github-line class="opacity-50"/>
  <div><a href="https://github.com/Subramanyarao11" target="_blank">subramanyarao11</a></div>
  <ri-twitter-line class="opacity-50"/>
  <div><a href="https://twitter.com/Subramanya11rao" target="_blank">subramanya11rao</a></div>
  <ri-user-3-line class="opacity-50"/>
  <div><a href="https://subramanyarao.hashnode.dev/" target="_blank">subramanyarao</a></div>
</div>



---
hideInToc: true
---

# Table of Content

<Toc listClass="!list-disc" maxDepth="2" />

---

# Intro to DOM

> The Document Object Model ( DOM ) defines the logical structure of documents and how a document is accessed and manipulated. It views an HTML document as a tree of nodes, where a node represents an HTML element.

<div v-click class="my-4">
With the <code>DOM</code> , JavaScript can access and change all the elements of an HTML document.
</div>

<div v-click class="my-6 text-2xl underline underline-offset-6 decoration-dotted">Visual Representation of DOM</div>

<div class="w-full flex items-center justify-center">
  <div v-click class="">
    <img class="h-70 pb-2" src="https://www.w3schools.com/js/pic_htmltree.gif">
  </div>
</div>

---
layout: content
---

# Why JavaScript ?

<div v-click>
<div class="text-lg text-gray-500">The Impact of JavaScript ( DOM ) in dynamic websites</div>

<div class="text-md my-4 py-2 px-2 border rounded-lg">
JavaScript plays a crucial role in enhancing the <span class="font-bold text-gray-100 underline light:text-gray-800">interactivity</span> and <span class="font-bold text-gray-100 underline light:text-gray-800">dynamic nature</span> of websites. Let's explore a few examples of how sites might behave without  JavaScript and then delve into creating dynamic elements using the DOM.
</div>
</div>


<div v-click class="my-8">
<a  target="_blank" href="https://www.netflix.com/in/" class="text-2xl">Netflix</a>
</div>

<div v-click class="my-8">
<a  target="_blank" href="https://hulu-clone-subramanya11.netlify.app/" class="text-2xl">Hulu Clone</a>
</div>

<div v-click class="my-8">
<a  target="_blank" href="https://www.jiocinema.com/" class="text-2xl">Jio Cinema</a>
</div>

<blockquote v-click>
<div class="text-base">
Let's see a practical example on DOM Manipulation & Event Handling by building Interactive and Dynamic Components
</div>
</blockquote>

---

# Example 1 : Dynamic Text
Dynamically update a paragraph text using `click` event
<div class="grid grid-cols-2 gap-x-4">

<v-clicks :every='1'>

<!-- parent div for 1st col -->
<div class="col-span-1">
<!-- HTML section start -->
<div>

###### index.html

```html
<div class="container">
  <p id="demo">Click the button to change this text.</p>
  <button id="changeTextBtn">Change Text</button>
</div>
```

<br>
</div>
<!-- HTML section ends -->


<!-- CSS Section starts -->
<div>

###### styles.css

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  margin: 0;
}

.container {
  text-align: center;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
```
</div>
<!-- CSS Ends -->
</div>
<!-- 1st col ends -->


<!-- 2nd col starts -->
<div class="col-span-1">

###### index.js

```ts
const changeTextButton = document.getElementById('changeTextBtn');
const demoParagraph = document.getElementById('demo');

changeTextButton.addEventListener('click', function () {
  demoParagraph.textContent = 'Text changed!';
});
```

</div>
<!-- 2nd col ends -->

</v-clicks>

</div>

---

# Example 2 : Modal Component
Dynamically display and hide a modal component using DOM Manipulation

<div class="grid grid-cols-2 gap-x-4 h-full">
<v-clicks :every='1'>
<div class="col-span-1 h-fit">
<!-- HTML section start -->

###### index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="styles.css">
  <title>Modal Example</title>
</head>
<body>

<button id="openModalBtn">Open Modal</button>

<div id="myModal" class="modal">
  <div class="modal-content">
    <span class="close" id="closeModalBtn">&times;</span>
    <h2>Welcome to the Modal!</h2>
    <p>This is a simple modal example. Click the 'X' or outside the modal to close it.</p>
  </div>
</div>

<script src="script.js"></script>
</body>
</html>

```

<br>
</div>
<!-- HTML section ends -->

<div class="col-span-1">
<!-- CSS section start -->

###### styles.css

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  margin: 0;
}

.modal {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  background-color: #fefefe;
  margin: 15% auto;
  padding: 20px;
  border: 1px solid #888;
  width: 80%;
  max-width: 600px;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}
```

<br>
</div>
</v-clicks>
</div>


---
hideInToc: true
---


# Example 2 : Modal Component
Dynamically display and hide a modal component using DOM Manipulation

###### script.js

```ts
const openModalBtn = document.getElementById('openModalBtn');
const modal = document.getElementById('myModal');
const closeModalBtn = document.getElementById('closeModalBtn');

// Open the modal
openModalBtn.addEventListener('click', function() {
  modal.style.display = 'block';
});

// Close the modal when clicking the close button or outside the modal
closeModalBtn.addEventListener('click', function() {
  modal.style.display = 'none';
});

window.addEventListener('click', function(event) {
  if (event.target === modal) {
    modal.style.display = 'none';
  }
});

```
---
hideInToc: false
---

# Comparing DOM Trees
Check the difference in DOM tree before and after DOM manipulation

---
hideInToc: false
---

# Some more events...
Few more events to explore and play around

<div class="grid grid-cols-2 gap-x-4">

###### Index.html

###### Index.js

<v-clicks :every='3'>

```html
<div class="container" id="mousemoveContainer">
  <p id="mousemoveText">Move your mouse to see magic!</p>
</div>
```

```ts
const mousemoveContainer = document.getElementById('mousemoveContainer');
const mousemoveText = document.getElementById('mousemoveText');

mousemoveContainer.addEventListener('mousemove', function(event) {
  const x = event.clientX;
  const y = event.clientY;
  mousemoveText.textContent = `Mouse Position: X - ${x}, Y - ${y}`;
});

```

</v-clicks>

<v-clicks :every='4'>

###### Index.html

###### Index.js

```html
<input id="textBox" type="text" />
<div id="output"></div>
```

```ts
const textBox = document.querySelector("#textBox");
const output = document.querySelector("#output");
textBox.addEventListener("keydown", (event) => {
  output.textContent = `You pressed "${event.key}".`;
});
```
</v-clicks>
</div>

---
hideInToc: false
---

# Additional Resources
Few more resources to learn more about DOM Manipulation and Event Handling

[Javascipt HTML DOM](https://www.w3schools.com/js/js_htmldom.asp)

[Javascipt DOM Manipulation](https://www.freecodecamp.org/news/dom-manipulation-in-javascript/)

[Manipulating Documents](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents)

[Important DOM Manipulation Methods](https://codevoweb.com/important-dom-manipulation-methods-in-javascript/)

[Introduction to Events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

[Javascipt Event Handlers](https://www.freecodecamp.org/news/javascript-event-handlers/)


---
hideInToc: true
layout: statement
---

# Thanks.

<twemoji-evergreen-tree class="text-4xl"  />
<twemoji-evergreen-tree class="text-4xl"  />
<twemoji-woman-superhero class="text-4xl player"  />
<twemoji-evergreen-tree class="text-4xl"  />
<twemoji-evergreen-tree class="text-4xl"  />
<twemoji-evergreen-tree class="text-4xl"  />
<twemoji-alien-monster class="text-3xl alien"  />
<twemoji-evergreen-tree class="text-4xl"  />

<style>
  @keyframes buzz {
    0% {
      transform: translateX(0px) rotate(0deg);
    }
    50% {
      transform: translateX(5px) rotate(12deg);
    }
    100% {
      transform: translateX(0px) rotate(0deg);
    }
  }

  .alien {
    animation: buzz 900ms infinite ease-in-out;
  }

  @keyframes breeth {
    0% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-1px);
    }
    100% {
      transform: translateY(0px);
    }
  }

  .player {
    animation: breeth 1500ms infinite ease-in-out;
  }
</style>
