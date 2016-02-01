# OpenFin Application window closing example
This is a vanilla JavaScript app seed for developing OpenFin apps. It is free from frameworks and build systems, though you may add them as you see fit.

It has a simple Node/Express server for local development.

Clone the repo and run

```
$ npm install
```
NB: on a Mac you may need to type 'sudo npm install'

Navigate to the root folder where 'server.js' resides with your command line tool and run:

```
$ node server
```

This should start a simple Node server at [http://localhost:3030](http://localhost:3030), then, click the link below to install as an openFin app.

If you wish to change to localhost port you will need to change the references in "server.js", "app.json" and in the installer link below.

[installer](https://dl.openfin.co/services/download?fileName=window_closing&config=http://localhost:3030/app.json)

Things to note. 

Avoid reusing the API call 'fin.desktop.Window.getCurrent()' when spawning applications. Use it once, when the app is created, and store a reference in a variable. This will avoid referencing the wrong app.

App creation is asynchronous, therefore, returning the new App via a Promise is good practice.
 
 