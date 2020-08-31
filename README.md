# onethird.skeleton

**Table of contents**

* <a href='#introduction'>Introduction</a>
* <a href='#goals'>Goals</a>
* <a href='#overview'>Overview</a>
* <a href='#file-layout'>File layout</a>
* <a href='#file-layout-visual'>File layout (visual)</a>
* <a href='#install'>Install</a>
* <a href='#source'>Source</a>

## <a id='introduction'>Introduction</a>

This repository is intended as an aid in Chrome extension development.
It provides a skeleton you can use to kickstart development of a new
extension that has a focus on content scripts.

## <a id='goals'>Goals</a>

The end goal is to create a number of skeletons that target different types
of Chrome extensions, for example those who only use content scripts all the way
to those who have content scripts, a background page, and a browser action. Or
different combinations of all three.

I hope to provide skeletons that have an option to use webpack and other build
tools as well as having skeletons that do not use them, and for that to be a feature
because that model of development can be simpler.

## <a id='overview'>Overview</a>

* This skeleton is designed for an extension that injects content scripts
  onto web page(s). It doesn't provide for anything beyond that like setting
  up the extension to have a browser action, or background page.

* This skeleton follows a model where the extension doesn't need to be "built".
  The source HTML, CSS and JS files are not processed by build tools in anyway.
  This approach provides simplicity. For example, in this environment you can
  edit the source and see the changes in the browser without a build step in
  between.

* An objective of this skeleton is to be loadable without edits
  being made. You can try loading it in Chrome first (with Developer Mode turned on),
  then edit afterwards if you want. This allows writing code before you decide
  a project name or which icons you'll use.

## <a id='file-layout'> File layout </a>

**JavaScript**

* The [`src/js`](src/js) directory is for JavaScript belonging to your extension.

* The [`src/js/content-scripts/`](/src/content-scripts) directory is for content 
  scripts belonging to your extension.

* The [`src/js/content-scripts/content-script.js`](src/js/content-scripts/content-script.js) is
  provided as a starting point to help with quick development.

**Images**

* The [`src/images`](/src/images) directory holds placeholder icons that the browser will
  display alongside the address bar and on the `chrome://extensions` page.

## <a id='file-layout-visual'> File layout (visual) </a>

      $ tree
      .
      ├── README.md
      └── src
          ├── images
          │   ├── icon128.png
          │   ├── icon16.png
          │   └── icon48.png
          ├── js
          │   └── content-scripts
          │       └── content-script.js
          ├── LICENSE.txt
          └── manifest.json

## <a id='install'> Install </a>

The install process is simple. All you have to do is clone the project and
then adopt it as the starting point for your new extension.

    git clone https://github.com/rg-3/onethird.skeleton my-project-name
    cd my-project-name
    # Make room for your own repository
    rm -rf .git
    # Make room for your own README
    mv README.md README.skeleton.md

## <a id='source'>Source</a>

The project homepage for this skeleton is at [https://github.com/rg-3/onethird.skeleton](https://github.com/rg-3/onethird.skeleton).
I am maintaining other Chrome extension skeletons that might be useful on my [github profile](https://github.com/rg-3).