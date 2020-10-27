# SASS

- Repository name: `sass-challenge`
- Mode: `solo`
- Type of Challenge: `exercise`
- Duration: `2 days`
- Deployment strategy: GitHub Pages

## Learning objectives

Sure, CSS is cool, but sometimes it can feel cumbersome. For example, what if _peach_ ([#ffe5b4](https://www.colorhexa.com/ffe5b4)) is your website's primary color, and it appears in multiple places in your CSS file, but suddenly the designer has a change of mind and she wants _lime green_ ([#b4ffe5](https://www.colorhexa.com/b4ffe5)) now? In how many different places do you have to make the correction? SASS will come to your rescue.

By the end of this challenge you will be able to:

- understand what a CSS preprocessor is, and why it exists
- generate some CSS from your CSS preprocessor (the industry standard is SASS/SCSS)
- be able to combine multiple SASS files into a single final CSS file
- be able to minify your CSS output

You will use the following SASS features:

- Variables
- Mixins (think functions)
- Nesting
- Partials & Import
- Extend/Inheritance
- Operators (math)

## The Mission

Your company prepared a SASS guide that uses old school CSS for styling. It doesn't make much sense, does it? Your mission is to rewrite `style.css` to a SCSS file.

But first, be sure to read the included `index.html` file for more information.

### Installation

To get started, install SASS with the instructions found on https://sass-lang.com/install  
After the installation type `sass -v` in the terminal, it should display the latest version.

#### PhpStorm

If you are using PhpStorm, the moment you create a `.scss` file, it will offer you to manage SASS compilation for you, you can accept this. In PhpStorm this is called a file watcher, you can always edit the settings in `file -> settings -> file watcher -> scss`.

<details>
    <summary>(Optional) Make Phpstorm write .css file to different directory</summary>

On default Phpstorm writes your CSS file to the same directory as your SCSS file.
In a bigger project you probably want to write your CSS files to a different directory like css/ to keep everything organised.

You can do that with the following changes in `file -> settings -> file watcher -> scss`:

- Arguments:  
   `--no-cache --update $FileName$:$ProjectFileDir$/css/$FileNameWithoutExtension$.css`

- Output path to refresh:
  `$ProjectFileDir$/css/$FileNameWithoutExtension$.css:$FileNameWithoutExtension$.css.map`

</details>

#### Visual Studio Code

If you are using VS Code you can install the [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass) extension. It will watch your SASS/SCSS files and automatically generate the CSS output.

#### Other editors

If you are using another editor you have to run commands from the terminal to watch and compile the files:

`sass --watch input.scss output.css (single file)`

`sass --watch app/sass:public/stylesheets (entire directory)`

### Instructions

#### Part 0

Copy the files `index.html` and `style.css` in your new repo. These are your reference files.

#### Part 1 - a lot of possibilities

Don't rush for the solution here. Take your time to try out the different possibilities SASS is granting you.

- A. _Nest_ the styling rules of grouped elements, like the `section`s in the `article`.
- B. Make one _mixin_ for the 3 lines of the box-shadow styling.
- C. Use one _variable_ for the general padding value that you see in multiple places (Note: the footer `h6` has double the padding of the other elements. Use _math operations_ to calculate it).
- D. Make use of _extend_ to re-use the same CSS for the "success", "error" and "warning" messages.

#### Part 2 - the tricky part!

- In the HTML, add 2 links called "blue" & "red".
- Clicking one of the 2 links should change the text to red/blue with a good matching background (keep it readable)!  
  Note: the rest of the CSS should be the same and should not be repeated, to do this you will have to use SASS variables and file imports.

Take some time to think how to do the structure of this second part (you will probably need additional files _wink wink_). It might be good to discuss this with your fellow juniors!

#### Part 3 (optional)

- Add an option to your compilation script to minify your stylesheet!  
  Mine was below 1.6k, can you do better? Do you still remember the option to `ls` to make the filesize Human readable?

## Good Luck!

![](https://media.giphy.com/media/VewtA3Qfk3Xih4E4Ii/giphy.gif)

## Wait, SCSS, SASS, what? What's the difference? Why sometimes `a` and sometimes `c`? I'm confused.

Well, **Sass** is the official name of the preprocessor (other preprocessors are **Less**, and **Stylus**).

You can write **Sass** files using two different (but similar) syntaxes. The most evident difference is that one (SCSS) uses curly brackets `{}`, and the other (SASS) uses indentation.

The **Sass** compiler knows which syntax you chose looking at the extension of the file (`.sass` or `.scss`).

The SCSS syntax is more similar to the CSS you are used to, so we recommend you start from it. You can always experiment with the SASS syntax later, and decide which one you prefer.

Example `style.sass`:

```sass
main
  background: #f4f4f4

  h1
    font-size: 24px

  p
    font-size: 18px
```

Example `style.scss`:

```scss
main {
  background: #f4f4f4;

  h1 {
    font-size: 24px;
  }

  p {
    font-size: 18px;
  }
}
```

![](./images/sassy.gif)
