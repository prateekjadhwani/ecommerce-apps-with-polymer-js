# What is an Element

I have been talking about widgets created using Web Components for quite some time now. But since the we can create these widgets as our own custom elements, let's just call them **elements** to make it simple. Polymer JS does the same job of creating custom elements. And just every Polymer module will be called as an Element for the sake of simplicity.

This way, even the smallest module or view can be thought of as an element. An element with its own functionality. Say for example, the `<star-rating></star-rating>` widget we talked about. First of all, instead of calling it as widget, we will be calling it as `<star-rating>` element. Secondly, since its only use is to store the rating value of a photo, we can limit its functionality to just displaying the stars and storing that value.

We can also think of a big module as an element. An element can include unlimited elements. Let me explain this with the help of an example. Let's say your page is supposed to show photos and star ratings of your portfolio, you can think of each row as its own element.This `<row>` element contains `<photo>` element and `<star-rating>` element with its own CSS styles on how to display the `<photo>` and `<star-rating>` elements in a row. And every row can be binded to a particular image. So even if you change the rating, it will change the rating of the image in the selected row. 

**insert image of row element**

> The reason I am using a lot of examples is because `elements` need a new way of think than traditional web apps.
