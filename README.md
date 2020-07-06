# Joplin Theme Playground   
The goal of this project is to construct the new theme and use it as an opportunity to refresh the CSS structure.

https://discourse.joplinapp.org/t/desktop-new-design-is-nearly-ready-please-cast-your-final-vote/9698/43

# tl;dr
You can see the theme in action from `index.html` in the public folder

## themes
All the themes were built off the base theme, changing the variables.

## screenshots
### base theme
![base-theme](/screenshots/base-theme.png)

### dark mode
![dark-mode](/screenshots/dark-mode.png)


### dark mode w/ overrides
in this example, all the navigation elements are moved to the bottom
![dark-mode](/screenshots/dark-mode-overrides.png)

### southwest
I'm not advocating for this theme, mostly showing that its really fast to take any color palette and derive a theme. This was a random palette from [http://coolors.co](http://coolors.co)
![southwest](/screenshots/southwest.png)

### monochrome
another random example, in this case I also simplified the indenting
![monochrome](/screenshots/monochrome.png)

Note: The base theme design was done by a different designer, I am just implementing the CSS. More info here: [designer discussion](https://discourse.joplinapp.org/t/joplin-new-design-feedback-is-welcome-20-june-update-version-4-is-ready/9324/36?u=uxamanda)


## how this playground is built
For speed of dev, I am using pug and sass, the render folder has the working files. the public folder has the output.


### simple server
to get everything linking nicely I run a python simple server in public file
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

## 0.0.1
initial push
