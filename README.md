# Joplin Theme Playground   
Goal is to look into the new theme and use it as an opportunity to refresh the CSS structure

## stack
For speed of dev, I am using pug and sass, the render folder has all the basics.
### html (pug)
to render pug to html. anytime you add a new .pug you need to restart
`pug render/pug --out public -w -P`

### css (sass)
this uses a custom fish script, i can publish if needed
`start_sass --sass="render/sass/" --css="public/css/"`

### simple server
to get everything linking nicely i run a python simple server of the public file
`python -m SimpleHTTPServer 8002`

## 0.0.1
initial push
