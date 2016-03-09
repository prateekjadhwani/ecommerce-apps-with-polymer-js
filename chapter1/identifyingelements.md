# Identifying Elements In a Web App

Let say your graphic designer just gave you a layout of how the web app should look like. And this is what he gave you.

![Screenshot](https://raw.githubusercontent.com/prateekjadhwani/ecommerce-apps-with-polymer-js/master/assets/identifying-elements-web-app.png)
This is a screenshot from my other project [SVG2CSS](https://prateekjadhwani.github.io/svg2css/) which creates `CSS` animation keyframes from SVG graphs.

Getting back to the topic, let's say this is what was provided to you. Now you have to break down your layout into different / seperate functional elements; this is what I personally would have done. 

- First divide the Web App into two separate elements, **header** and **container**. **Header**, where the non-relevant information related to the project is avaialble; and **Container** where the main content of the app is placed.
- **Header** can further be broken down into other inner elements. 
  - **Title** can be considered as an element; whose main job is to display the title. 
  - **Help Button**; whose main job is to open the help page/documentation. 
  - **Bug Icon**; to help users submit an issue.
  - **Save Icon** to save the code on `gist.github.com`
  - **Github Buttons** which show details about the project.
- Inside **Container** elements, we can have other elements as well
  - **SVG-Keyframe** just to display an SVG, get property inputs from the user and convert those inputs into SVG keyframes.
  - **Code Editor** to help the user write code. We can see `html` and `css` editors in the layout, soo we can have a single element with different modes.
  - **Live Preview** to see the output of the code that user wrote.
 
Now that we have all the major elements identified, I would like to point out one important thing. Not every element is what it looks like. There is a lot of background functionality added to elements to make it work as a functional unit. 

For example the **Save Icon** element. It's main purpose is to save the code and keyframes generated to [gist.github.com](https://gist.github.com/). That would only happen if the user is authenticated, hence the element is also reponsible for authenticating a user via github, then using the oAuth token to create a new gist, and save to that gist. The element is also responsible for updating the gist with users new changes. An example of Multiple business logics falling into the same functional unit.

Another example would be **Code Editor** element. We can see that there is some code written in then editor element. And the code has been parsed and various keywords have different color based on what language it is. In technical terms, that would mean that your element would need different parsing rules for different languages without changing the overall functionality. This made me create a new variable called `mode` which keeps a track of the language that editor is supposed to display. When `mode` is `css`, it can use different rule, and when `mode` is `html` it can use different rule. An example of code reuse.

This was just a small example of what could be considered an element in a layout. Identifying elements comes with lots of practice. As I told you in the previous topics that Polymer uses a totally different mindset, this practice of identifying every element on the screen / layout is an important part of that mindset.
