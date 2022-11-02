# Custom Right Click Context Menu in HTML CSS & Javascript

This is a simple custom context menu that can be accessed by right-clicking inside the page and disappears when left-clicked inside the page. Within the selections, it can also have sub-menus.

This context menu consists of 3 files to function:

```
  1.  index.html
  2.  style.css
  3.  script.js
```

##  index.html

HTML is a text-based approach to describing how content contained within an HTML file is structured. This file sets up on how the menu will look like (with content) on the page.

A class is a space-separated list of the classes of the element. Classes allows CSS and JavaScript to select and access specific elements via the class selectors or functions like the method Document.getElementsByClassName(). The .html file has several class used:

  1.  wrapper - Specifies how the text in a text area is to be wrapped when submitted in a form.
  2.  content - Gives the value associated with the http-equiv or name attribute.
  3.  menu    - Appears upon user interaction, such as a right-click. HTML now allows us to customize this menu.
  4.  item    - List down the items the user can interact within the menu.

The html code should be constructed as per below:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>
            Custom Context Menu
        </title>
        <link rel="stylesheet" href="style.css">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="https://unicons.iconscout.com/release/v4.0.0/css/line.css">
    </head>
    <body>
        <div class="wrapper">
            <div class="content">
                <ul class="menu">
                    <li class="item">
                        <i class="uil uil-eye"></i>
                        <span>Preview</span>
                    </li>
                    <li class="item share">
                        <div>
                            <i class="uil uil-share"></i>
                            <span>Share</span>
                        </div>
                        <i class="uil uil-angle-right"></i>
                        <ul class="share-menu">
                            <li class="item">
                                <i class="uil uil-twitter-alt"></i>
                                <span>Twitter</span>
                            </li>
                            <li class="item">
                                <i class="uil uil-instagram"></i>
                                <span>Instagram</span>
                            </li>
                            <li class="item">
                                <i class="uil uil-dribbble"></i>
                                <span>Dribble</span>
                            </li>
                            <li class="item">
                                <i class="uil uil-telegram-alt"></i>
                                <span>Telegram</span>
                            </li>
                        </ul>
                    </li>
                    <li class="item">
                        <i class="uil uil-link-alt"></i>
                        <span>Get Link</span>
                    </li>
                    <li class="item">
                        <i class="uil uil-edit"></i>
                        <span>Rename</span>
                    </li>
                    <li class="item">
                        <i class="uil uil-trash-alt"></i>
                        <span>Delete</span>
                    </li>
                </ul>
                <div class="setting">
                    <li class="item">
                        <i class="uil uil-setting"></i>
                        <span>Settings</span>
                    </li>
                </div>
            </div>
        </div>
        <script src="script.js"></script>
    </body>
</html>
```

##  style.css

CSS stands for 'Cascading Style Sheets'. CSS describes how HTML elements are to be displayed on screen, paper, or in other media. CSS saves a lot of work. It can control the layout of multiple web pages all at once. External stylesheets are stored in CSS files.

With proper consideration for formatting and a sprinkle of a bit of creativity, one could come up with a context menu looking like this one below:

![Screenshot_1](images/Screenshot_20221102_110316.png)

First off, we style the fonts to be used for this interface. Any existing fonts are suitable to use. However, I choose to import a font provided by GoogleAPI. These are the choices of formats below:

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
```

Next, we move on with styling the body tag:

```css
body
{
    min-height: 100vh;
    background: linear-gradient(135deg, #8855E9 0%, #5D6BE6 100%);

}
```

Then, we style the wrapper that hold our app:

```css
.wrapper
{
    position: absolute;
    visibility: hidden;
    width: 300px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 12px 35px rgba(0,0,0,0.1);
}

.wrapper .menu
{
    padding: 10px 12px;
}

```
