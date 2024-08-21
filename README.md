# CSS-Variables-Hamburgers

![ScreenRecording](https://github.com/TomoyaKuroda/CSS-Variables-Hamburgers/assets/31934952/6a059ca4-25dd-427e-b50a-2fd0da2a0713)

This is an open-source project inspired by [Hamburgers](https://jonsuh.com/hamburgers/), but with the customization feature of using CSS variables instead of Sass. With this project, you can easily create stylish hamburger menu animations for your web projects using pure CSS.

## Motivation

The motivation behind this project is to provide a simpler and more flexible alternative to using Sass for customizing hamburger menu animations. By utilizing CSS variables, developers can easily tweak colors, sizes, and other properties directly in their CSS files without the need for Sass preprocessing.

## Features

- Easy-to-use hamburger menu animations.
- Customizable with CSS variables.
- Lightweight and dependency-free.
- Cross-browser compatible.

## Usage

1. Download the CSS file ```css-variable-hamburgers.min.css```.
2. Include the CSS file in your HTML document:

```html
<link rel="stylesheet" href="css-variable-hamburgers.min.css">
<!-- CDN -->
<link href="https://cdn.jsdelivr.net/npm/@tomoyakuroda/css-variables-hamburgers@1/css-variables-hamburgers.min.css" rel="stylesheet">
```

3. Add the base hamburger markup:

```html
<button class="hamburger" type="button">
  <span class="hamburger-box">
    <span class="hamburger-inner"></span>
  </span>
</button>  
```

4. Append the class name of the type of hamburger you’re craving:

```html
<button class="hamburger hamburger--collapse" type="button">
  <span class="hamburger-box">
    <span class="hamburger-inner"></span>
  </span>
</button> 
```

5. Customize the hamburger menu using CSS variables:

```css
:root {
  --hamburger-padding-x           : 15px;
  --hamburger-padding-y           : 15px;
  --hamburger-layer-width         : 40px;
  --hamburger-layer-height        : 4px;
  --hamburger-layer-spacing       : 6px;
  --hamburger-layer-color         : #000;
  --hamburger-layer-border-radius : 4px;
  --hamburger-hover-opacity       : 0.7;
  --hamburger-active-layer-color  : var(--hamburger-layer-color);
  --hamburger-active-hover-opacity: var(--hamburger-hover-opacity);
}
```

6. Toggle the hamburger menu animation with JavaScript.

```js
<script>
  // Look for .hamburger
  var hamburger = document.querySelector(".hamburger");
  // On click
  hamburger.addEventListener("click", function() {
    // Toggle class "is-active"
    hamburger.classList.toggle("is-active");
    // Do something else, like open/close menu
  });
</script>
```

## Contributing

Contributions are welcome! If you have any ideas for improvements or new features, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License.

## Acknowledgments

- Inspired by [Hamburgers](https://github.com/jonsuh/hamburgers) by [Jonathan Suh](https://github.com/jonsuh).
- Built with love and CSS variables.
