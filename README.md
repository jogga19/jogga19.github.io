# simple-static-website-template
A template for getting started with personal, static websites.
Template was found at [simple-static-website-template](https://github.com/edavis0/simple-static-website-template)

## Overview
This repo provides a beginner-level starting place for users to create their own static websites. It's inspired by and built using [Derek Siver's simple website template](https://sive.rs/ti#web1). Feel free to clone it and build your own static website, and if you found this helpful, take a second to **star ✩ this repo**!

## How to get started
1. Clone or download this repo locally on your machine.
2. Find `index.html` in your file explorer, and then open it in your browser.
3. As changes are made to `index.html` or any child pages, simply refresh the page to visualize the changes.

That's it! You can now see the template in your browser. To get started, I recommend looking at the `index.html` template, playing around with it, and then referring back to this README.

## Quick Note on the Folder Structure
If you downloaded or cloned this repo, you'll have one directory above the `website` directory: `simple-static-website-template`. Once you've built your website and you're ready to make it live, you should delete the `simple-static-website-template` top-level directory and associated files (`README.md`, etc.).

## How to modify `index.html`
`index.html` should live at the top-level of your directory tree. It's your homepage. This is where you'll want to start building on the template. Here are a few good places to get started.

### Modify the title tag
The `<title>` tag in HTML is used to specify the title of the webpage. This title is displayed on the title bar of the web browser or in the page tab for tabbed browsers. It's also typically used when bookmarking a page and is displayed in search engine results. The `<title>` tag is placed within the head section of the HTML document, as the head section is where metadata about the document, like the title and links to CSS stylesheets, is usually placed.

Modify your title tag to reflect the title and site address of your website's home page. `<title>PAGE TITLE HERE | SITE NAME HERE</title>` -> `<title>Home | mywebsite.com</title>`

### Modify the `<h1>` header
The `<h1>` tag, similar to the `#` symbol in Markdown, creates a large header on your webpage. I recommend combining it with an anchor tag that is linked to your homepage. Example: `<h1><a href="index.html">SITE NAME HERE</a></h1>` -> `<h1><a href="index.html">mywebsite</a></h1>`.

Alternatively, you can remove the anchor tag, and just create an unlinked header like this: `<h1>SITE NAME HERE</h1>`.

### Add content
Now that you've added page meta data and a top-level header, you're ready to add content!

To begin, you may want to divide your page into multiple sections. You can use header tags of varying size to do so. Header tags like `<h2>` and `<h3>` allow you to create headers of smaller sizes (i.e. `<h3>` is smaller than `<h2>`).

Once you've added headers, it's time to get writing! Before you create a paragraph, insert a `<p>` tag. This signifies the beginning of a paragraph, and it creates a line break. Traditionally, HTML uses a `<p>` tag to start a paragraph and a `</p>` tag to end a paragraph. If you're just getting started, though, this may be a little hard to read. You can simply use `<p>` tag to create line breaks in your text. Here's an example.

HTML code:
```
<p>
This is my first paragraph.
<p>
This is my second paragraph.
```
Page render:
```
This is my first paragraph.

This is my second paragraph.
```

## How to manage page linkage
Often, you'll want to provide your readers with links that allow them to go back to your higher-level pages like `index.html` and `now.html` from pages that are further down the directory tree, such as your individual blogs. You can do that with HTML anchor elements and relative path symbols.
- Anchor elements can be inserted anywhere in your HTML code using the following format `<a href="link">display-text</a>`.
    - `<a>`: this is the opening tag for an anchor element.
    - `href="link"`: this is an attribute of the `<a>` tag that specifices the URL or file that the reader will be taken to when they click the link.
    - `display-text`: this is the text that will be displayed as the hyperlink on the webpage.
    - `</a>:` this is the closing tag for the anchor element.
- The `./` symbol is a shorthand symbol for the current directory.
- The `../` symbol is a shorthand symbol for the parent directory relative to the current directory.

For example, your directory is likely structured like the following:
```
simple-static-website-template
│   README.md
│   Additional repo files, directories, etc.
│
└───website
    │   index.html
    │   now.html
    │   style.css
    │
    └───blog
        │ blog.html
        │
        └───YYYY
            │ blog1.html
            │ blog2.html

```
You can provide linkage between pages using anchor tags and relative file path symbols:
- If you need to link from `now.html` to `index.html`, you can use the following anchor tag: `<a href="./index.html"index</a>`. 
- If you need to linke from `blog1.html` to `index.html`, you can use the following anchor tag: `<a href="./../../index.html"index</a>`.

## How to manage page style
You can modify `style.css` to visually change your webpages however you like. This template uses a slightly modified version of the CSS file from [Derek Siver's simple website template](https://sive.rs/ti#web1), but it's very bare-bones. I recommend doing some Google searching to decide how to style your own pages.