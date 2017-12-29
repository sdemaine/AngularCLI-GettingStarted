
\ng new my-sassy-app --style=scss
sass folder structure
sass
 |__ abstracts
    |__ _functions.scss
    |__ _mixins.scss
    |__ _variables.scss
 |__ base
    |__ _animations.scss
    |__ _base.scss
    |__ _typography.scss
    |__ _utilities.scss
 |__ components
    |__ _button.scss
 |__ layout
    |__ _grid.scss
    |__ _header.scss
 |__ pages
    |__ _home.scss
 |__ themes
    |__ _default.scss
 |__ vendors

 main.scss
 
 -- command to make this directory structure
 md sass && cd sass && md abstracts && md base && md components && md layout && md pages && md themes && md vendors && echo // main.scss > main.scss && cd abstracts && echo // _function.scss > _function.scss && echo // _mixins.scss > _mixins.scss && echo // _variables.scss > _variables.scss && cd.. && cd base && echo // _animations.scss > _animations.scss && echo // _base.scss > _base.scss && echo // _typography.scss > _typography.scss && echo // _utilities.scss > _utlities.scss && cd.. && cd components && echo // _button.scss > _button.scss && cd.. && cd layout && echo // _grid.scss > _grid.scss && echo // _header.scss > _header.scss && cd.. && cd pages && echo // _home.scss > _home.scss && cd.. && cd themes && echo // _default.scss > _default.scss && cd..  

[contents of main.scss] 
################################
@import 'abstracts/functions';
@import 'abstracts/mixins';
@import 'abstracts/variables';

@import 'base/animations';
@import 'base/base';
@import 'base/typography';
@import 'base/utilities';

@import 'components/button';

@import 'layout/grid';
@import 'layout/header';

@import 'pages/home';


// import only the parts of bootstrap that we intend to use with the following syntax
@import 
  '~bootstrap/scss/functions',
  '~bootstrap/scss/variables',
  '~bootstrap/scss/mixins',
  '~bootstrap/scss/print',
  '~bootstrap/scss/reboot',
  '~bootstrap/scss/type';


################################


update .angular-cli.json
"styles": [
  "sass/main.scss"
],
"stylePreprocessorOptions": {
  "includePaths": [
    "my-path"
  ]
},

// includePaths are searched by sass when it attempts to find imported files

## How to import sass files into Angular component
@import '~sass/variables';
// The tilde (~) will tell Sass to look in the src/ folder and is a quick shortcut to importing Sass files.              