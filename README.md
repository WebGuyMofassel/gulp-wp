# gulp-wp

Custom gulp packages for quick WordPress theme development.

# Required gulp plugin list with installation command:

# gulp
    sudo npm install --save-dev gulp
# gulp-plumber
    npm install --save-dev gulp-plumber

# gulp-ruby-sass
    sudo npm install --save-dev gulp-ruby-sass

# gulp-autoprefixer
    sudo npm install --save-dev gulp-autoprefixer

# gulp-uglify
    sudo npm install --save-dev gulp-uglify

# gulp-livereload
    sudo npm install --save-dev gulp-livereload

NB: sudo = super user do, permision required. You may need to delete README.md file to avoid any issue, if you want to add additional plugin with the repo.

# Additional gulp basic:

#Step 1: 
    sudo apt-get update
    sudo apt-get install nodejs

#Step 2: nodejs package manager installation.
    sudo apt-get install npm

#Step 3: Install gulp globally.
    npm install --global gulp 
#OR 
    sudo npm install -g gulp

#Step 4: Create project folder say gulp-project and create a json file named package.json
    touch package.json
    // just put {} inside newly created file
#Step 5: install and save gulp for your local project devDependencies
    npm install --save-dev gulp

#Step 6: Create a gulpfile.js at the root of your project.
    
    var gulp = require('gulp');
    
    gulp.task('default', function() {
      // place code for your default task here
    });

#Step 7: Run gulp: though now output will be nothing

    gulp

#Step 8: Adding plugin with gulp. http://gulpjs.com/plugins/
    npm install --save-dev plugin-name

#Step 9: Few frequently needed plugin list 

    gulp-ruby-sass 
    gulp-autoprefixer
    gulp-plumber
    gulp-uglify
    gulp-livereload

#Step 10: Adding plugin support in gulpfile.js file.
    var gulp = require('gulp');
    var sass = require('gulp-ruby-sass');
    
    gulp.task('sass', function() {
        return sass('source/') 
        .on('error', function (err) {
          console.error('Error!', err.message);
       })
        .pipe(gulp.dest('result'));
    });

    gulp.task('default', function() {
      // place code for your default task here
    }); 
