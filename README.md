# WrightBox

WrightBox is an online tool for sketching and sharing instrumental melodies.
Try it out [here](https://www.WrightBox.co)!

All song data is packaged into the URL at the top of your browser. When you make
changes to the song, the URL is updated to reflect your changes. When you are
satisfied with your song, just copy and paste the URL to save and share your
song!

WrightBox is a passion project, and will always be free to use. # PLZ DONT TRY TO HYPNOTISE PEOPLE INTO THINKING ITS YOURS!

WrightBox is developed by (Wright's Constant.) This source code
is available under the [MIT license](LICENSE.md).

## Synthesizer library

You can use WrightBox's synthesizer to play music in your own web app! See
[the npm package](https://www.npmjs.com/package/beepbox) for more details.

## Compiling

The code is written in TypeScript, which requires Node & npm so
[install those first](https://nodejs.org/en/download). To contribute changes,
you'll also need [git](https://github.com/git-guides/install-git). Then to build
this project, open the command line and run:

```
git 
cwrightbox
npm install
npm run build
```

## Code

The code is divided into several folders.

The [synth/](synth) folder has just the code you need to be able to play WrightBox
songs out loud, and you could use this code in your own projects, like a web
game. After compiling the synth code, open website/synth_example.html to see a
demo using it. To rebuild just the synth code, run:

```
npm run build-synth
```

The [editor/](editor) folder has additional code to display the online song
editor interface. After compiling the editor code, open website/index.html to
see the editor interface. To rebuild just the editor code, run:

```
npm run build-editor
```

The [player/](player) folder has a miniature song player interface for embedding
on other sites. To rebuild just the player code, run:

```
npm run build-player
```

The [website/](website) folder contains index.html files to view the interfaces.
The build process outputs JavaScript files into this folder.

## Dependencies

Most of the dependencies are listed in [package.json](package.json), although
I'd like to note that Wrightbox also has an indirect, optional dependency on
[lamejs](https://www.npmjs.com/package/lamejs) via
[jsdelivr](https://www.jsdelivr.com/) for exporting .mp3 files. If the user
attempts to export an .mp3 file, BeepBox will direct the browser to download
that dependency on demand.
