# Shower Slideshow!

Built using [middleman](middlemanapp.com) and shower (http://github.com/pepelsbey/shower)

## How to Install
      
First install middleman

    gem install middleman

Then install the middleman-shower template (installs to `~/.middleman/shower`)

    mkdir -p ~/.middleman
    cd ~/.middleman
    git clone git://github.com/railsjedi/middleman-shower.git shower
  
you only need to do this once. Update the git repo every once in a while to grab the latest template

    cd ~/.middleman/shower
    git pull
  
## How to use
  
This will allow you to create a new project using the shower slideshow template

    middleman init my_new_slideshow --template=shower
    
Learn more about middleman here: [http://middlemanapp.com/](http://middlemanapp.com/)
        

## How to Build
  
    middleman build

this outputs the build folder to build/, copy this to any static folder to deploy your slideshow


## Autodeploy to Github

    rake github:deploy
    
## Source

See it here: [http://github.com/railsjedi/middleman-shower](http://github.com/railsjedi/middleman-shower)
