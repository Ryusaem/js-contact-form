# Frontend Mentor - Contact form

![Design preview for the Contact form coding challenge](./design/desktop-preview.jpg)

[Challenge - Contact Form](https://www.frontendmentor.io/challenges/contact-form--G-hYlqKJj)

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

**To do this challenge, you need a good understanding of HTML, CSS and JavaScript.**

Your challenge is to build out this contact form and get it looking as close to the design as possible. Pay particular attention to making this form accessible. Building accessible forms is a key skill for front-end developers. So this is a perfect challenge to practice.

You can use any tools you like to help you complete the challenge. So if you've got something you'd like to practice, feel free to give it a go.

Your users should be able to:

- Complete the form and see a success toast message upon successful submission
- Receive form validation messages if:
  - A required field has been missed
  - The email address is not formatted correctly
- Complete the form only using their keyboard
- Have inputs, error messages, and the success message announced on their screen reader
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

template
![Screenshot Project](/design/screenshot.png)

### Links

- Solution URL: [GitHub](https://github.com/Ryusaem/js-contact-form)
- Live Site URL: [Github Live Demo](https://ryusaem.github.io/js-contact-form/)

## My process

Total:

    - design/wireframe: xx min
    - coding/implementation: xx min
    - documentation/README.md: xx min
    - total: xx minutes

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- JavaScript
- TO ADD OR REPLACE

### What I learned

1. A screen reader will speak an asterisk as "star" when encountered. When hovered by a sighted mouse user, "required" should appear, which is achieved by use of the title attribute....Titles being read aloud depends on the screen reader's settings, so it is more reliable to also include the "aria-label" attribute, which is always read by screen readers.

2. As you can see in the examples, it's common practice to wrap a label and its widget with a <li> element within a <ul> or <ol> list. <p> and <div> elements are also commonly used. Lists are recommended for structuring multiple checkboxes or radio buttons.

3.In addition to the <fieldset> element, it's also common practice to use HTML titles (e.g. h1, h2) and sectioning (e.g. <section>) to structure complex forms.

4.Above all, it is up to you to find a comfortable coding style that results in accessible, usable forms. Each separate section of functionality should be contained in a separate <section> element, with <fieldset> elements to contain radio buttons.

5.Accessibility: Add aria-label attributes to improve accessibility for screen readers.

```html
<label for="name">Name:</label>
<input
  type="text"
  id="name"
  name="name"
  aria-label="Name"
/>
```

6.  The common input types button, checkbox, file, hidden, image, password, radio, reset, submit, and text.

7.  For maximum usability/accessibility, you are advised to surround each list of related items in a <fieldset>, with a <legend> providing an overall description of the list. Each individual pair of <label>/<input> elements should be contained in its own list item (or similar). The associated <label> is generally placed immediately before or after the radio button or checkbox, with the instructions for the group of radio button or checkboxes generally being the content of the <legend>. See the examples linked above for structural examples.

8.  Related checkbox items should use the same name attribute. Including the checked attribute makes the checkbox checked automatically when the page loads. Clicking the checkbox or its associated label toggles the checkbox on and off.

9.  Due to the on-off nature of checkboxes, the checkbox is considered a toggle button, with many developers and designers expanding on the default checkbox styling to create buttons that look like toggle switches. You can see an example in action here (also see the source code).

10. Several radio buttons can be tied together. If they share the same value for their name attribute, they will be considered to be in the same group of buttons. Only one button in a given group may be checked at a time; this means that when one of them is checked all the others automatically get unchecked. When the form is sent, only the value of the checked radio button is sent. If none of them are checked, the whole pool of radio buttons is considered to be in an unknown state and no value is sent with the form. Once one of the radio buttons in a same-named group of buttons is checked, it is not possible for the user to uncheck all the buttons without resetting the form.

11. The image button control is rendered exactly like an <img> element, except that when the user clicks on it, it behaves like a submit button.
    An image button is created using an <input> element with its type attribute set to the value image. This element supports exactly the same set of attributes as the <img> element, plus all the attributes supported by other form buttons.

        ```html
        <input
          type="image"
          alt="Click me!"
          src="my-img.png"
          width="80"
          height="30"
        />
        ```

        If the image button is used to submit the form, this control doesn't submit its value — instead, the X and Y coordinates of the click on the image are submitted (the coordinates are relative to the image, meaning that the upper-left corner of the image represents the coordinate (0, 0)). The coordinates are sent as two key/value pairs:

        The X value key is the value of the name attribute followed by the string ".x".
        The Y value key is the value of the name attribute followed by the string ".y".

        So for example when you click on the image at coordinate (123, 456) and it submits via the get method, you'll see the values appended to the URL as follows:
        url

        http://foo.com?pos.x=123&pos.y=456

        This is a very convenient way to build a "hot map". How these values are sent and retrieved is detailed in the Sending form data article.

        - File picker

        There is one last <input> type that came to us in early HTML: the file input type. Forms are able to send files to a server (this specific action is also detailed in the Sending form data article). The file picker widget can be used to choose one or more files to send.

        To create a file picker widget, you use the <input> element with its type attribute set to file. The types of files that are accepted can be constrained using the accept attribute. In addition, if you want to let the user pick more than one file, you can do so by adding the multiple attribute.

        ```html
        <input type="file" name="file" id="file" accept=".jpg, .jpeg, .png" multiple>
        ```

        - for mobile

```html
<input
  type="file"
  accept="image/*;capture=camera"
/>
<input
  type="file"
  accept="video/*;capture=camcorder"
/>
<input
  type="file"
  accept="audio/*;capture=microphone"
/>
```

- Note: If the data entered is not an email address, the :invalid pseudo-class will match, and the validityState.typeMismatch property will return true.
- A slider is created using the <input> with its type attribute set to the value range. The slider-thumb can be moved via mouse or touch, or with the arrows of the keypad.
- It's important to properly configure your slider. To that end, it's highly recommended that you set the min, max, and step attributes which set the minimum, maximum, and increment values, respectively.

```html
<label for="price">Choose a maximum house price: </label>
<input
  type="range"
  name="price"
  id="price"
  min="50000"
  max="500000"
  step="100"
  value="250000"
/>
<output
  class="price-output"
  for="price"
></output>
```

- One problem with sliders is that they don't offer any kind of visual feedback as to what the current value is. This is why we've included an <output> element to contain the current value. You could display an input value or the output of a calculation inside any element, but <output> is special — like <label> — and it can take a for attribute that allows you to associate it with the element or elements that the output value came from.

```javascript
const price = document.querySelector("#price");
const output = document.querySelector(".price-output");

output.textContent = price.value;

price.addEventListener("input", () => {
  output.textContent = price.value;
});
```

still a lot of thigns to learn...added this sentence for little commit message

-

```html
<!-- EXMAPLE code block -->
```

### Continued development

- TO ADD

### Useful resources -

[Frontend Mentor](https://www.frontendmentor.io/challenges/) - Formidable resources to make you learn by "doing" awesome project. Highly recommend it.

## Author -

- Github - [@Ryusaem](https://github.com/Ryusaem) -
- Linkedin - [@sambath-meas](https://www.linkedin.com/in/sambath-meas)
- Coursera - [@sambath-meas](https://www.coursera.org/learner/sambath-meas)
- Twitter - [@RyuBraveheart](https://twitter.com/RyuBraveheart) - - - Frontend Mentor - [@Ryusaem](https://www.frontendmentor.io/profile/Ryusaem)
- CodeWars - [@Ryusaem](https://www.codewars.com/users/Ryusaem)
