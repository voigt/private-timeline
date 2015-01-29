
#Creating a Dev-Environment

Not sure what is the best approach to start. I saw that yeoman has an node-webkit generator. Since we commited to use node-webkit I thought it would be a good idea to test it :)

This is how the installation process worked (for me). I also selected all available OS environments in order to give the best support for other OSs.

> *Attention*  
> After installing generator-node-webkit I needed to change a file in `node_modules/generator-node-webkit/download/index.js`. Due to the renaming of node-webkit to nw you need to change lines `21` and `22` which declare the download URL. Please change all occurrences of `dl.node-webkit.org` to `dl.nwjs.io`.

```
$ npm install -g yo
$ npm install -g generator-node-webkit # installing nw generator for yo
$ #npm install generator-node-webkit   # for only installing it locally to the directory

christophs-mbp:private-timeline cv$ yo node-webkit

     _-----_
    |       |
    |--(o)--|   .--------------------------.
   `---------´  |    Welcome to Yeoman,    |
    ( _´U`_ )   |   ladies and gentlemen!  |
    /___A___\   '__________________________'
     |  ~  |
   __'.___.'__
 ´   `  |° ´ Y `

? What do you want to call your app? Allowed characters ^[a-zA-Z0-9]+$ privateTimeline
? A little description for your app? A private timeline, reading your Day One entries.
? Would you mind telling me your username on GitHub? voigt
? Do you want to install one of the node-webkit examples? Yes
     info Get GitHub informations
✔ Github informations successfully retrieved.
     info Getting list of available examples.
? Which example do you want to install? file-explorer
   invoke   node-webkit:download
? Do you want to download node-webkit? Yes
? Please specify which version of node-webkit you want download: (v0.10.5) 
     info     Check if version "v0.10.5" is available for download.
? Please specify which version of node-webkit you want download: v0.10.5
? Which platform do you wanna support? MacOS 32, MacOS 64, Linux 64, Linux 32, Windows
     info     Creating folder structure for node-webkit source.
✔ Created: "resources/node-webkit"
✔ Created: "resources/node-webkit/MacOS32"
✔ Created: "resources/node-webkit/MacOS64"
✔ Created: "resources/node-webkit/Linux64"
✔ Created: "resources/node-webkit/Linux32"
✔ Created: "resources/node-webkit/Windows"
✔ Created: "tmp"
     info     Downloading node-webkit for MacOS32
     info     Downloading node-webkit for MacOS64
     info     Downloading node-webkit for Linux64
     info     Downloading node-webkit for Linux32
     info     Downloading node-webkit for Windows
✔ Node-webkit for Windows downloaded
✔ Node-webkit for Linux64 downloaded
✔ Node-webkit for Linux32 downloaded
✔ Node-webkit for MacOS32 downloaded
✔ Node-webkit for MacOS64 downloaded
     info     Unzip MacOS32 files.
     info     Unzip MacOS64 files.
     info     Un.tar.gz Linux64 files.
     info     Un.tar.gz Linux32 files.
     info     Unzip Windows files.
✔ "tmp/Windows.zip" successfully unzipped
✔ "tmp/MacOS32.zip" successfully unzipped
✔ "tmp/MacOS64.zip" successfully unzipped
✔ Linux64 directory successfully copied.
✔ Linux32 directory successfully copied.
     info Downloading node-webkit examples
     info Unzip examples.
✔ Examples successfully unzipped
   create .editorconfig
   create .jshintrc
 conflict .gitignore
? Overwrite .gitignore? overwrite
    force .gitignore
   create bower.json
   create resources/mac/dmgStyler.applescript
   create resources/mac/package.sh
   create resources/mac/background.png
   create package.json
   create Gruntfile.js
   create resources/mac/Info.plist.tmp
   create resources/mac/Info.plist

I'm all done. Running bower install & npm install for you to install the required dependencies. If this fails, try running the command yourself.


npm WARN package.json privatetimeline@0.0.0 No description
npm WARN deprecated deflate-crc32-stream@0.1.2: module has been merged into crc32-stream
npm WARN prefer global yo@1.4.5 should be installed with -g

> yo@1.4.5 postinstall /Users/cv/github.com/private-timeline/node_modules/yo
> yodoctor


Yeoman Doctor
Running sanity checks on your system

✔ No .bowerrc file in home directory
✔ Global configuration file is valid
✔ NODE_PATH matches the npm root
✔ No .yo-rc.json file in home directory

Everything looks all right!
grunt-contrib-copy@0.5.0 node_modules/grunt-contrib-copy

grunt-contrib-rename@0.0.3 node_modules/grunt-contrib-rename

grunt-contrib-clean@0.6.0 node_modules/grunt-contrib-clean
└── rimraf@2.2.8

concat-files@0.1.0 node_modules/concat-files
└── async@0.2.10

grunt-contrib-concat@0.5.0 node_modules/grunt-contrib-concat
├── source-map@0.1.43 (amdefine@0.1.0)
└── chalk@0.5.1 (ansi-styles@1.1.0, escape-string-regexp@1.0.2, supports-color@0.2.0, strip-ansi@0.3.0, has-ansi@0.1.0)

time-grunt@0.4.0 node_modules/time-grunt
├── date-time@0.1.1
├── figures@1.3.5
├── text-table@0.2.0
├── hooker@0.2.3
├── chalk@0.5.1 (escape-string-regexp@1.0.2, ansi-styles@1.1.0, supports-color@0.2.0, strip-ansi@0.3.0, has-ansi@0.1.0)
└── pretty-ms@0.2.2 (parse-ms@0.1.2)

load-grunt-tasks@0.6.0 node_modules/load-grunt-tasks
├── multimatch@0.3.0 (array-differ@0.1.0, array-union@0.1.0, minimatch@0.3.0)
└── findup-sync@0.1.3 (lodash@2.4.1, glob@3.2.11)

grunt@0.4.5 node_modules/grunt
├── which@1.0.8
├── dateformat@1.0.2-1.2.3
├── eventemitter2@0.4.14
├── getobject@0.1.0
├── rimraf@2.2.8
├── colors@0.6.2
├── async@0.1.22
├── hooker@0.2.3
├── grunt-legacy-util@0.2.0
├── exit@0.1.2
├── nopt@1.0.10 (abbrev@1.0.5)
├── minimatch@0.2.14 (sigmund@1.0.0, lru-cache@2.5.0)
├── lodash@0.9.2
├── coffee-script@1.3.3
├── underscore.string@2.2.1
├── glob@3.1.21 (inherits@1.0.0, graceful-fs@1.2.3)
├── iconv-lite@0.2.11
├── findup-sync@0.1.3 (glob@3.2.11, lodash@2.4.1)
├── js-yaml@2.0.5 (argparse@0.1.16, esprima@1.0.4)
└── grunt-legacy-log@0.1.1 (underscore.string@2.3.3, lodash@2.4.1)

grunt-contrib-compress@0.10.0 node_modules/grunt-contrib-compress
├── prettysize@0.0.3
└── archiver@0.9.1 (buffer-crc32@0.2.5, lazystream@0.1.0, readable-stream@1.0.33, tar-stream@0.3.3, zip-stream@0.3.7, lodash@2.4.1, file-utils@0.1.5)

grunt-contrib-jshint@0.10.0 node_modules/grunt-contrib-jshint
├── hooker@0.2.3
└── jshint@2.5.11 (strip-json-comments@1.0.2, underscore@1.6.0, exit@0.1.2, minimatch@1.0.0, shelljs@0.3.0, console-browserify@1.1.0, cli@0.6.5, htmlparser2@3.8.2)
```

##Okay, where to go from here?

Yeoman installed a lot of stuff and a working example. To get the example working read [this](https://github.com/Dica-Developer/generator-node-webkit/wiki/Getting-Started) generator-node-webkit wiki page.

In order to build the web app you need to install the grunt build tool:

```
$ sudo npm install -g grunt-cli # again, -g for globally!
$ grunt dist-mac # if there are to many js-hint errors use --force
```

Finally you should find a `privateTimeline.app` in `dist/MacOS64`. The source of the example app can be found in `app/`.