# Joplin Theme Playground   
The goal of this project is to construct the new theme and use it as an opportunity to refresh the CSS structure.

https://discourse.joplinapp.org/t/desktop-new-design-is-nearly-ready-please-cast-your-final-vote/9698/43

# tl;dr
1. You can see the themes in action by downloading and viewing the public folder.
2. Switch the themes by changing the `index.html` file at `line 8`
3. If you cannot see the icon font, see the "simple server" instructions below.

## Themes
All the themes were built off the base theme, generally just changing the variables.

## screenshots
### base theme
![base-theme](/screenshots/base-theme.png)

### dark mode
![dark-mode](/screenshots/dark-mode.png)


### southwest
I'm not advocating for this theme, mostly showing that its really fast to take any color palette and derive a theme. This was a random palette from [http://coolors.co](http://coolors.co)
![southwest](/screenshots/southwest.png)

### monochrome
another random example, in this case I also simplified the indenting
![monochrome](/screenshots/monochrome.png)



### dark mode w/ overrides
This is the most complex example. In here, all the navigation elements are moved to the bottom by using a different note grid definition.
![dark-mode](/screenshots/dark-mode-overrides.png)

Note: The base theme design was done by a different designer, I am just implementing the CSS. More info here: [designer discussion](https://discourse.joplinapp.org/t/joplin-new-design-feedback-is-welcome-20-june-update-version-4-is-ready/9324/36?u=uxamanda)


## how this playground is built
For speed of dev, I am using pug and sass, the render folder has the working files. the public folder has the output.


### simple server
to get everything linking nicely I run a python simple server from the command line
```bash
cd public
python -m SimpleHTTPServer 8002
```


### html (pug)
to render pug to html. anytime you add a new ``.pug` file you need to restart
```bash
pug render/pug --out public -w -P
```

### css (sass)
this uses a custom fish script, i can publish if needed
```bash
sass --update --force  render/sass/:public/css/
                sass --watch render/sass/:public/css/
```

SASS Structure
- `_base_layout` - this is the main structure of the body and the sidebars
- `_note_layout` - this is the structure of the note panel
- `_colors` - defines colors throughout
- `_typography` -  defines type throughout
- `_actions` - defines buttons, search, and the fancy todo checkboxes

You'll notice that because it is broken up like this, you get the same classes defined more than once. I have found it much easier to work on large projects when the css is split in this way, since you are generally working on type at once, then color, etc. When they are split by class, it is harder to keep the styles tight.


# Commit History
## 0.0.1
initial push
