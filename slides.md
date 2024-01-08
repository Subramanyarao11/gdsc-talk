---
layout: cover
download: https://antfu.me/talks/2021-04-29
highlighter: shiki`
title: DOM & Event Handling in JS
coverAuthor: Subramanya Rao
titleTemplate: '%s - Subramanya Rao'
---

# DOM Manipulation and Event Handling

Introduction to DOM Manipulation and Event Handling in Javascript

<div class="uppercase text-sm tracking-widest">
Subramanya Rao
</div>

<div class="abs-bl mx-14 my-12 flex">
  <img src="https://res.cloudinary.com/startup-grind/image/upload/c_fill,dpr_2.0,f_auto,g_center,h_1080,q_100,w_1080/v1/gcs/platform-data-dsc/events/logo_QTdLJEf.jpg" class="h-8 mt-2">
  <div class="ml-3 flex flex-col text-left">
    <div><b>Frontend</b> Workshop @ GDSC, RNSIT</div>
    <div class="text-sm opacity-50">Jan. 11th, 2024</div>
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
layout: 'intro'
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
layout: table-of-contents
---

# Agenda

---

# Intro to DOM

> The DOM defines the logical structure of documents and how a document is accessed and manipulated. It views an HTML document as a tree of nodes, where a node represents an HTML element.

With the `HTML DOM` , JavaScript can access and change all the elements of an HTML document.

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
JavaScript plays a crucial role in enhancing the <span class="font-bold text-gray-100 underline light:text-gray-800">interactivity</span> and <span class="font-bold text-gray-100 underline light:text-gray-800">dynamic nature</span> of websites. Let's explore a few examples of how sites might look without JavaScript and then delve into creating dynamic elements using the DOM.
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
Let's see a practical example on DOM Manipulation & Event Handling by building a Interactive and Dynamic Component
</div>
</blockquote>

---
    