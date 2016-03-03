# Introduction

Every thing that will be done in Polymer JS is dependent on a really important concept called **Web Components**. So, I would like to take a moment here and talk about Web Components. In layman's term, a web component is more like a widget created using Various Web Technologies and can be reused n number of times on a webpage.

The most common example of a web component would be, say you want a rating system for all the photos on your site. So you decided to create a 5 star voting widget. You will have multiple instances of this rating widget and the user can click any of the 5 stars to give you the rating for a particular picture.

**insert a pic of a webpage with ratings on images**

In terms of frontend coding, wouldn't it be nice if this widget could be a DOM element called `<star-rating></star-rating>` that can be used to store the values from `1` to `5`. The element is intelligent enough to understand what the attribute `value` is and has events like `onChange()` just like any other input field. These all features can be attained with the help of Web Components.

In technical terms, Web Component is merely a concept attained by interactions of a bunch of Web Technologies that can even be used separately or independent of each other. The web technologies used in creating a web component are as follows:

#### Shadow DOM

When we talk about widgets made out of `HTML`, `JavaScript` and `CSS` there is always a problem of encapsulation. What it means is, if you have a widget that uses a `div` with a class name `.container` and you decided to have the `background` of this class as `red` that would mean, anywhere on the page if there is a class `.container` it will also have a red background. Off course you can take care of it by specifically targeting particular divs based on long class names, but the question is, how many long class names are you willing to write or how many `!important` keywords will you be adding. And we haven't even talked about JavaScript events yet.

So, in order to attain this encapsulation, the concept of Shadow DOM was introduced. This simply creates a document node instead of an element node. This way, a Shadow DOM doesn't leak out the data related to its inner elements. We just need to remember that Shadow DOM provides encapsulation, but if you would like to know more information on Shadow DOM, feel free to refer the (Shadow DOM W3C Editor's Draft](https://w3c.github.io/webcomponents/spec/shadow/).

#### Custom Elements

Custom Elements cover the concept of naming your widget to a custom html tag. This way, a widget can be named as a new type of `HTML` tag and can be used just like any other normal DOM with all the DOM apis.

#### HTML Imports

Just the way you can include scripts and css via `<script>` and `<link rel="stylesheet">` tags, HTML imports had to be created so that html files can be included in another html. This is mostly useful when you want one widget to include another widget. We will be dicussing HTML imports in detail when we start talking about Polymer JS, but for now we just need to understand what this concept is for.

#### HTML Templates

Any type of content that doesn't need to be rendered on initial page load but can be added later on is called a template. These templates are mostly added with  the help of JavaScript. In HTML, this can be attained with the help of HTML templates or the `<template>` tags.