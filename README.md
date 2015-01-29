
#Creating a Dev-Environment

Not sure what is the best approach to start. I saw that yeoman has an node-webkit generator. Since we commited to use node-webkit I thought it would be a good idea to test it :)

[This](https://github.com/voigt/private-timeline/wiki/How-the-App-was-bootstrapped) is how the installation process worked (for me). I also selected all available OS environments in order to give the best support for other OSs.



How to compile.
===============

First, clone this repository.

```
https://github.com/voigt/private-timeline.git
```

Next, go download a suitable version of [node-webkit](https://github.com/rogerwang/node-webkit).

Copy node-webkit into the node-webkit/ folder

```
$ cd ~/github.com/private-timeline/
$ mkdir -p resources/node-webkit
$ cp ~/Downloads/node-webkit/* ~/github.com/private-timeline/resources/node-webkit
```

Install the Node dependencies

```
$ cd ~/github.com/private-timeline/
$ npm install
```

## Building the application

To test your app you have to build a distribution from it. Depending on your development system you have to use one of the following grunt tasks.

On a linux call
[source,bash]
$ grunt dist-linux # for 64bit
$ grunt dist-linux32 # for 32bit

On a pc call
[source,bash]
$ grunt dist-win

On a mac call
[source,bash]
$ grunt dist-mac # for 64bit
$ grunt dist-mac32 # for 32bit

The resulting application can then be found in the folder dist.

## Running the application

You can run it now with the following commands depending again on your dev platform.

On a linux call
[source,bash]
$ cd dist
$ ./node-webkit myfirstnwapp.app

On a mac call
[source,bash]
$ dist/MacOS64/myfirstnwapp.app/Contents/MacOS/node-webkit

Combine creation and starting the app in one line with grunt

On a linux call
[source,bash]
$ grunt dist-linux && cd dist && ./linux64/node-webkit myfirstnwapp.app

On a mac call
[source,bash]
$ grunt dist-mac && dist/MacOS64/myfirstnwapp.app/Contents/MacOS/node-webkit


## Structure

The node-webkit-generator creates the following folders.
[format="csv",cols="2"]
[options="header"]
|======
Folder,What is it for?
app,This is the folder where your node-webkit application will be go in. After first initialization there will be an hello world application inside. You can structure it how you want. The requirement is that the package.json file is directly in the app folder.
resources,This folder stores files necessary to build different distributions from your application e.g. the node-webkit binaries.
|======
