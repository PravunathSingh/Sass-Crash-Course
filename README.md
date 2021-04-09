## Sass Crash Course

Sass (short for syntactically awesome style sheets) is a preprocessor scripting language that is interpreted or compiled into Cascading Style Sheets (CSS). SassScript is the scripting language itself.

Sass consists of two syntaxes. The original syntax, called "the indented syntax," uses a syntax similar to Haml. It uses indentation to separate code blocks and newline characters to separate rules. The newer syntax, "SCSS" (Sassy CSS), uses block formatting like that of CSS. It uses braces to denote code blocks and semicolons to separate rules within a block. The indented syntax and SCSS files are traditionally given the extensions .sass and .scss, respectively.

#### Features of Sass:

- Makes writing variables easy. Instead of the traditional syntax "--variable-name: value;" we can just use "$variable-name: value".
- Allows nesting. Eg:

```
  showcase-content {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;

    img {
      width: 50%;
    }

    h1 {
      font-size: 50px;
      line-height: 1.2;
    }

    p {
      margin: 20px 0;
    }
  }
```

- Allows use of mixins and functions.
- Allows Inheritance using the @extend keyword.
- Using Sass we can apply logic or conditionals in our CSS.
- Partials, i.e instead of having a huge monolithic code for all our CSS, we can break up our CSS into chunks and then import them in our main styles.css file.

### The following repo consists of a small part of a basic landing page styled using Sass.

- styles.scss is the main Sass file.
- \_config.scss files are generally used to add variables, functions, mixins etc.
- \_utilites.scss file are generally used to add common utility classes like containers, cards, dropdowns, buttons, forms. etc.
- \_mobile.scss file contains the media queries for the responsiveness.

#### To include Sass in your project follow these steps:

- Make a Sass / scss folder and create a styles.scss file.
- Install the Live Sass Compiler extension.
- Go to setting > live sass compiler > edit in json; and add the following code

```
"liveSassCompile.settings.formats": [
        {
            "format": "compressed",
            // "extensionName: ".min.css,
            "savePath": "/css"
        }
    ],
    "liveSassCompile.settings.generateMap": false,
```

Note: the savePath can be changed as per your preference.

- Finally click on Watch Sass button at the bottom right corner.

### To learn more about various features, rules of Sass and additional methods of installing Sass visit [here] (https://sass-lang.com/) .
