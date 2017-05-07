# AngularCliExample

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.0.2.

## It is aimed to show how to load an angular project as a GH page.

See https://carmelc.github.io/angular-cli-example/dist/index.html for a running example.

There are two ways to be able to run an Angular static project as a Github Page:

1. Use the Master branch (shown in this example but considered as a 'dirty' way)
   1. Remove dist folder (or any other output folder used in runtime) from .gitignore file
   2. Run your build
   3. Push your changes
   4. make sure that the index.html file in your runtime folder (dist folder in this repo) does not define base ur in the <head> section. If there is such definition, remove it.
You can see how was it done in [this commit](https://github.com/carmelc/angular-cli-example/commit/d83e38881ad327e1ae3855795d3037cdc934bb97)
   5. In the repository Settings (top right of the page in github) in the *GitHub Pages* section, select master branch from the dropdown and click Save.
   6. Open https://{username}.github.io/{repo-name}/{path to index.html}/index.html 

2. Create a dedicated branch called gh-pages
   1. Create a new branch called gh-pages (git checkout -b gh-pages)
   2. Delete content of .gitignore file (do not ignore any file)
   3. Delete all the sources from the main folder
   4. Copy the content of the products directory (e.g. dist in Angular CLI) into the main folder, make sure that the index.html file is in the root folder
   5. In the repository Settings (top right of the page in github) in the *GitHub Pages* section, select your branch from the dropdown and click Save.
   6. open https://{username}.github.io/{repo-name}
