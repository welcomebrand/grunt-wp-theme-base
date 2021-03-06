***Please note: I no longer actively support this theme*** 

You are more than welcome to continue using it and making changes if you wish but due to time commitments and general lack of WordPress use in my current work it's not something I can help with if any issues arise. 

Thanks!

#Using the Starter Kit

##Things you need to install

It's assumed you've already got Ruby and Sass installed. If you haven't, get them installed first along with:

* Node.js and Grunt (see above)

##It's now Grunt powered

It's Grunt powered so you need to install Node.js and Grunt [Here are the getting started instructions](http://gruntjs.com/getting-started) or [some other install instructions](http://24ways.org/2013/grunt-is-not-weird-and-hard/).

##Getting set up in your working directory / theme folder

You will need to install the various Grunt tasks we use so in terminal navigate to directory, run `npm install` and then install our packages as follows:

###The basic tasks it performs are:

**Minifies JS and then concatenates all the files into a single file**

If you need to add new JS files to the project, simply drop them into /js/app/ and Grunt does the rest.

You don't need to reference them in the HTML, Grunt will run the task and compile them all into production.js

For the time being, files in /js/libs/ need referencing in HTML and are not processed in Grunt.

**Image optimisation**

Any images located in /assets/images/ (jpg, png, gif) are automatically optimised and re-saved with the same name/paths when Grunt is run

**Sass compiling**

All files in /assets/sass/ are automatically compiled and minified and then output to /assets/css/screen.css which is referenced in the HTML

Do not under any circumstances edit /assets/css/screen.css, any changes you make will be lost next time Sass is compiled.

If you need to add a new scss file for some reason, you can do so by creating a _yourfilename.scss file (the underscore is needed) and you can then reference that in /assets/sass/screen.scss and it'll compile next time Grunt runs.

**CSS Prefixing**

You don't need to include browser specific prefixing for properties, they're automatically added when Grunt compiles the
Sass so just add un-prefixed properties and if they're needed it's taken care of.

**SVG fallbacks to PNG**

If you create any SVG assets for the project - icons etc, save them to /assets/images/svg/ and Grunt will generate a PNG version of the same size to use as a fallback in your CSS.
