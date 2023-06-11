# London Scientific
London-scientific is a custom theme for scientists, based on Ghost's
[London-Theme](https://london.ghost.io)

In 2019 I have commissioned to Simon Bernard a Ghost blog theme that was suited for scientists. I indicated the style and my personal workflow, and Simon coded this entirely.
Simon can no longer work on the project, and this is my fork of the theme, which I continue to adopt for [www.danieleaviatbile.com](www.danieleavitabile.com). 

# Usage

## Static homepage
To create a static front page with customized content please follow these steps:
1. Create a new page and give it a title
1. Change the Page URL of this page to "home" (in settings tab of the page)
1. Add some content to your page
1. Optionally: add a feature image to this page, the image will be rendered in a left column on the home page

This page is now shown as content on your home page.


## List of Publications
1. Create a new page and give it a title
1. Choose the Template "Publications" from the template list (bottom of settings tab of the page)
1. Give your page some optional content (will be shown above the post list)
1. Create a tag **for each** category in your publications list (eg. Books). The slug of this tag has to be in the form: "publication-x-books". Replace x with a number to define the order in which the categories should be listed (ascending).
1. Create any number of posts, each representing a publication. Assign those posts to one of the publication tags created in the last step (eg. "publication-books"). Give those posts a custom excerpt as this will be used to render the list items.
1. Create a link in your menu that points to your page created in step 1.


## List of Travels
Just follow steps 1 to 6 above. Replace each "publication" by "travel" (watch upper and lowercase).


## News section
To create a news page, follow these steps. A news page will show the latest 5 posts each of publications and travels categories.
1. Create a new page and give it a title (eg. News)
1. Choose the Template "News" from the template list (bottom of settings tab of the page)
1. Give your page some optional content (will be shown above the post list)
1. Create a link in your menu that points to your page created in step 1.

## Flat lists for easy conversion to CV
It is sometimes useful to turn pages with long list of publications and conferences
into text that can be copy and pasted for CVs or similar tasks. This is achieved by
injecting the following code

````
<script src="https://code.jquery.com/jquery-3.4.1.slim.min.js"></script> 
<script> 
const urlParams = new URLSearchParams(window.location.search); 
const plain = urlParams.get('plain'); 
$(document).ready(function () { 
$(".hide").toggleClass("hide", plain === "true"); 
}); 
</script> 
````

Calling, for instance http:www.danieleavitabile.com/list-of-publications/?plain=true
returns a flat list that can be copied.

# Copyright & License
Copyright 2018-2019 Simon Bernard - Released under the [MIT license](LICENSE).
