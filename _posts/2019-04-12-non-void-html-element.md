---
title: "Unclosed non-viod elements"
date: 2019-02-17
---

### Unclosed div element: Bug detected on timbu.com website [HNG Internship Stage two task]

W3C defines a void element as an element whose content model never allows it to have contents under any circumstances. [Read more](https://www.w3.org/TR/2011/WD-html-markup-20110113/syntax.html#void-element) 

The W3C [HTML validator](https://validator.w3.org) and [CSS validator](https://jigsaw.w3.org/css-validator/) was used to check the above mentioned [website](https://timbu.com/) after inspecting the live website using Google chrome dev tools.
The HTML validator caught 17 errors while the CSS validator caught 45 errors and 1732 warnings.

Out of these errors I chose to write about the unclosed div element.

The actual problem of not closing tags in HTML is majorly the unexpected ways content can be impacted.

In this particular example if the div element was meant to be styled in a unique way the result would have affected the content of the page as a whole.

[HTML Errors](https://validator.w3.org/nu/?doc=https%3A%2F%2Ftimbu.com%2F)
![HTML Errors](https://drive.google.com/uc?id=1Ze0a_EyUtduDWaxxLbzqqdZP_CAGf8HY)

[CSS Errors and Warnings](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Ftimbu.com%2F&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en#warnings)
![CSS Errors and Warnings](https://drive.google.com/uc?id=1_SWpOlkg8hr7N0_6OGK9rjqjtlj0J8uX)

`"HTML5 does not require empty elements to be closed. But if you want stricter validation, or if you need to make your document readable by XML parsers, you must close all HTML elements properly."` -[w3schools](https://www.w3schools.com/html/html_elements.asp)

`"Tag omission: A div element must have both a start tag and an end tag."` - [W3C Working Draft](https://www.w3.org/TR/2011/WD-html-markup-20110113/div.html#div)

It is best practice to always close [non-void element](https://www.w3.org/TR/2011/WD-html-markup-20110113/syntax.html#void-element) such as div, button, article, aside, h1-h6, form, figure, etc, despite the fact that it may not have an obvious effect.



##### This post was written as a qualifying requirement for [HNG Internship](https://hng.tech/).
