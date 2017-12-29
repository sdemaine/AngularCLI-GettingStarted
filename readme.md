#### Create initial app
```
ng new my-sassy-app --style=scss
```

#### Sass folder structure
>> *main.scss*
>> **abstracts**
>>> *_function.scss*
>>> *_mixins.scss*
>>> *_variables.scss*

>> **base**
>>> *_animations.scss*
>>> *_base.scss*
>>> *_typography.scss*
>>> *_utilities.scss*

>> **components**
>>> *_button.scss*

>> **layout**
>>> *_grid.scss*
>>>*_header.scss*

>> **pages**
>>> *_home.scss*

>> **themes**
>>> *_default.scss*

>> **vendors**

### Code to create sass folder structure
```
md sass && cd sass && md abstracts && md base && md components && md layout && md pages && md themes && md vendors && echo // main.scss > main.scss && cd abstracts && echo // _function.scss > _function.scss && echo // _mixins.scss > _mixins.scss && echo // _variables.scss > _variables.scss && cd.. && cd base && echo // _animations.scss > _animations.scss && echo // _base.scss > _base.scss && echo // _typography.scss > _typography.scss && echo // _utilities.scss > _utlities.scss && cd.. && cd components && echo // _button.scss > _button.scss && cd.. && cd layout && echo // _grid.scss > _grid.scss && echo // _header.scss > _header.scss && cd.. && cd pages && echo // _home.scss > _home.scss && cd.. && cd themes && echo // _default.scss > _default.scss && cd..
```


### contents of main.scss
```
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
```

##### import only the parts of bootstrap that we intend to use with the following syntax
##### (searches *node_modules*)
```
@import 
  '~bootstrap/scss/functions',
  '~bootstrap/scss/variables',
  '~bootstrap/scss/mixins',
  '~bootstrap/scss/print',
  '~bootstrap/scss/reboot',
  '~bootstrap/scss/type';
```

##### update .angular-cli.json
```javascript
"styles": [
  "sass/main.scss"
],
"stylePreprocessorOptions": {
  "includePaths": [
    "my-path"
  ]
},
```

#### How to import sass files into Angular component
##### (includePaths are searched by sass when it attempts to find imported files)
```
@import '~sass/variables';
```
The tilde (~) will tell Sass to look in the **src/** folder and is a quick shortcut to importing Sass files.      

#### Setting up AngularCLI debuggin in Visual Studio Code
https://github.com/Microsoft/vscode-recipes/tree/master/Angular-CLI


#### Github adding remote repository
https://help.github.com/articles/adding-a-remote/


Add remote repository

```
git remote add origin https://github.com/user/repo.git
```


Set Upstream Branch
```
git push --set-upstream origin master
```