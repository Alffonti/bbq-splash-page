# Concepts I've learned in this project

- Using text properties
    - The `line-height` property
    - The `text-transform` property
    - The `letter-spacing` property
- Using viewport units (vh adn vw) to cover the entire screen
- Adding background images to sections
- Using gradients with the `background: linear-gradient()` property
- Adding transitions to buttons and input elements (on hover and on focus psedudoelements)
- Blending modes (blending images with colors (or gradients))
    - Multiply (keep dark colors)
    - Screen (keep light colors)
    - Overlay
- Adding and styling forms (`<form action="#" method="POST">`)
    - Input (`<input type="text">`)
    - Button (`<button type="submit"></button>`)


## Wrapping the content on bigger screens

### Solution #1
setting a maxwidth to all the direct children of the intro and main-content section 

```
.intro > *,
.main-content > * {
    max-width: 400px;
    margin-left: auto;
    margin-right: auto;
}
```

### Solution #2
creating a container element inside the intro and main-content section; nesting all elements inside the container; applying the flex properties to the container instead of the intro section; matching the height of the container to the intro section height

```
.container{
    max-width: 400px;
    margin: 0 auto;
}

.container-intro{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 50vh;
}

@media (min-width: 500px) {
    .container-intro {
        height: 100%;
    }
}
```