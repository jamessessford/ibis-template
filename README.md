# Ibis Template

This is a template repository for [Ibis](https://github.com/themsaid/ibis) by [Mohamed Said](https://twitter.com/@themsaid).

To get started with this repository, please ensure you have Ibis installed on your system and it's a command that's registered on your path.

## Setup

### Config

Once you've forked the repo, you'll need to edit a couple of lines in the file ```ibis.php```

Set the title attribute to the title of the document.

Set the author attribute to the author of the document.

If you plan on releasing samples, update the sample generation array to the pages you want to include and update the sample notice at the bottom of the file.

### Assets

The repo contains the two themes provided by Ibis and the original cover image. It also contains a customizable ```cover.html``` file.

If you plan to use the cover file rather than the image, delete the image and update ```cover.html```, filling in the appropriate details for your project.

The included themes can be modified or you can create your own theme as ```theme-{name}.html```.

### Content

The content directory includes a logo image (which is used by the cover file) and ```000-changes.md``` which would be included as the first page of the produced document.

### VS Code

There are a few entries in the ```.vscode``` folder that are made to make writing your document easier.

This template recommends the installation of PDF Preview and Trigger Task on Save.

This allows me to split the panes in VS Code and have the content in one pane and the output PDF in another so I can see the changes I'm making in real time.

```tasks.json``` contains a reference to the build task for ibis which is triggered when either the cover file/cover image or markdown content in the ```content``` directory is changed.

The build task is triggering the default Ibis build command, which uses ```theme-light.html``` as its theme but can be changed to use other themes if required:

|Command|Theme|
|---|---|
|ibis build|theme-light.html|
|ibis build dark|theme-dark.html
|ibis build {name}|theme-{name}.html|
