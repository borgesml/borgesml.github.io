
![trial logo](Referenzobjekt 1.jpeg)

# WEBSITE TRIAL

## here is where we add what this website is about

Information Information Information [trial link](https://scholar.google.com/) via Google. 

## Table of Contents

- [Chapter 1](#Chapter-1)
- [Chapter 2](#Chapter-2)
- [Chapter 3](#Chapter-3)
- [Images](#images)
- [Styles](#styles)
- [Limitations](#limitations)
- [Todo](#todo)

## Chapter 1

TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT

TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT:

- **[Showdown JS](http://showdownjs.com/)** - for the conversion of Markdown to HTML
- **[Pico CSS](https://picocss.com/)** - to add (classless) default styles for the site
- **[Highlight JS](https://highlightjs.org/)** - to add syntax highlighting for code blocks

<details>
  <summary>This is an example of a toggle list</summary>
  
  ### Question goes up there
  1. Information 1
  2. Information 2
     * Information 2.1
     * Information 2.2

  ### Another question here
    1. Information 1
  2. Information 2
     * Information 2.1
     * Information 2.2
 </details>

  

## Chapter 2
### An attempt to create a table
|        Title 1             |          Title 2        |
| :---        |    :----:   |
|      Content Content 1         |       Content Content 2           |
|          Content Content 3          |        Content Content 4           |
| Content Content 5   | Content Content 6       |

Nice!

## Chapter 3

```
markdown-pages/
|---assets/
|------user/
|	   |---favicon.png
|	   |---example.png
|---pages/
|	|---sample-page.md
|	|---sample-page-2.md
|---index.html
|---README.md
```

### README.md

The `README.md` file will provide the content for the homepage of your site. Simply author the file using [Markdown syntax](https://www.markdownguide.org/basic-syntax/).

### index.html

The `index.html` file does the magic of converting Markdown to HTML. It will also look for a heading level 1 (h1) on the current page and prepend it to the site title. You can add your site title by modifying this line in the header:

```
&lt;title&gt;Markdown Pages&lt;/title&gt;
```

There are other lines in the header that you may want to edit as well, such as the meta description and the favicon image name/location.


### Pages

Additional pages can be added to the `pages` directory, using Markdown files. To add a link to an additional page, for example, `sample-page.md`, the following link structure can be used: 

```
Check out the [sample page](?page=sample-page)
```

Check out the [sample page](?page=sample-page) (link will work on the rendered site, not github.com).

### Assets

Images and other files can be added to the `assets/user` directory and linked as needed. 

## Images

Images can be included with Markdown as they normally are:

```
![markdown logo](assets/user/markdown.svg)
```

And image sizing configuration is available through the [parseImgDimensions](https://showdownjs.com/docs/available-options/#parseimgdimensions) option in Showdown JS:

```
![bar](bar.jpg =100x*)    sets width to 100px and height to "auto"
![foo](foo.jpg =100x80)   sets width to 100px and height to 80px
![baz](baz.jpg =80%x5em)  sets width to 80% and height to 5em
```

## Styles

### Dark/Light Mode

The site will include a dark/light mode toggle button by default. When adding images to a page, consider adding images that will contrast well against both a light and dark background.

### Syntax Highlighting

Syntax highlighting will automatically be applied to code blocks, for example:

```
def my_function():
  fruits = ['orange', 'apple', 'pear', 'kiwi', 'banana']
  for fruit in fruits:
    if fruit == 'banana':
        print(fruit)

my_function()
```

## Limitations

- **Local Development** - since the site uses XMLHttpRequest to grab content, a local web server will be needed if you want to test things locally, e.g. `python -m http.server`. However, editing files directly on a server/GitHub is part of the convenience/fun.
- **Limited element options** - if the element you're trying to use exists in Markdown, the converter should be able to render it as HTML, but this will exclude a lot of more advanced HTML elements.  
- **No custom layouts** - Markdown used in this way is fairly linear, so you won't be able to do a columns and fancy layouts without extra work.

## Todo

- Find/create a classless a11y CSS framework?
- Add a header/menu and footer section in `index.html` that can be populated from Markdown files?
- Escape HTML in code blocks using JS, so that this doesn't have to be done in code blocks to render correctly
- Implement more [Showdown JS options](https://github.com/showdownjs/showdown/wiki/Showdown-Options)
- Move pages out of 'pages' directory so that GitHub and hosted site can find assets using the same relative paths?
