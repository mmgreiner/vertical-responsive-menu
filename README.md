# PureCSS vertical responsive menu

I have been using [purecss] in most of my applications since it is really simple to use.

This is a small code sample that uses [purecss] with a responsive, vertical menu with hamburger and a submenu.

So it posed two challenges:
- responsive vertical menu with hamburger
- submenus


## Submenus

[purecss] does a fairly good job explaining how to do submenus in their documentation [Vertical Menu with Submenu](https://purecss.io/menus/#vertical-menu-with-submenus)

Unfortunately, this code did not show the submenu. It took me some time to understand the line:

~~~
<div class="pure-menu custom-restricted-width">
  <ul class="pure-menu-list">
  ...
</div>
~~~

The trick lies in the `custom-restricted-width`. I finally set this in the style sheet:

~~~css
.custom-restricted-width {
    display: inline-block;
}
~~~


## Responsive vertical menu

I took this example from the provided [purecss] layouts on [Side Menu](https://purecss.io/layouts/side-menu/#home), with the associated 
[styles.css](https://github.com/pure-css/pure/blob/master/site/static/layouts/side-menu/styles.css) and 
[ui.js](https://github.com/pure-css/pure/blob/master/site/static/js/ui.js).


## Caveats

I noticed that the style sheet sets the width of the vertical menu to `150px`. Just changing the width is not so simple, because then suddenly the hamburger disappears. This restricts the length of the menu texts, but I ended up not changing this.

## Usage

Just download the three files and open `simple_index_vertical_menu.html` in your favorite browser.



[purecss]: https://purecss.io/