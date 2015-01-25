Setting up a Node.js project
=========================

## Initialize a node.js project
Running ```npm init``` will create a package.json file. Answer the questions interactively. Remember to use app.js as entry point, as required by beanstalk.

```
(local-dev-env) $ npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sane defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg> --save` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
name: (test) shopXX-ierg4210
version: (1.0.0) 1.0.0
description: IERG4210 ShopXX
entry point: (index.js) app.js
test command: 
git repository: https://github.com/ierg4210/shopXX.git
keywords: education, CUHK, ierg4210, web programming and security, assignment, ecommerce
author: adon
license: (ISC) BSD
About to write to /Users/adon/projects/ierg4210/shopXX/package.json:

{
  "name": "shopXX-ierg4210",
  "version": "1.0.0",
  "description": "IERG4210 ShopXX",
  "main": "app.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/ierg4210/shopXX.git"
  },
  "keywords": [
    "education",
    "CUHK",
    "ierg4210",
    "web",
    "programming",
    "and",
    "security",
    "assignment",
    "ecommerce"
  ],
  "author": "adon",
  "license": "BSD",
  "bugs": {
    "url": "https://github.com/ierg4210/shopXX/issues"
  },
  "homepage": "https://github.com/ierg4210/shopXX"
}


Is this ok? (yes) yes
```

## Install the npm packages needed to run your project
Here shows an example on installing "express". With the ```--save``` parameter, this package will also be automatically marked as a dependency of your project. So, when beanstalk deploys your app by ```npm install```, the dependencies will be installed as well.
Check package.json after installation, and you will see something like ```"dependencies": {"express": "^4.11.1"}```. See ```$ npm help install``` for details.
```
(local-dev-env) $ npm install express --save
express@4.11.1 node_modules/express
├── merge-descriptors@0.0.2
├── utils-merge@1.0.0
├── methods@1.1.1
├── fresh@0.2.4
├── cookie@0.1.2
├── escape-html@1.0.1
├── range-parser@1.0.2
├── cookie-signature@1.0.5
├── finalhandler@0.3.3
├── media-typer@0.3.0
├── vary@1.0.0
├── parseurl@1.3.0
├── serve-static@1.8.1
├── content-disposition@0.5.0
├── path-to-regexp@0.1.3
├── depd@1.0.0
├── on-finished@2.2.0 (ee-first@1.1.0)
├── qs@2.3.3
├── debug@2.1.1 (ms@0.6.2)
├── proxy-addr@1.0.5 (forwarded@0.1.0, ipaddr.js@0.1.6)
├── etag@1.5.1 (crc@3.2.1)
├── send@0.11.1 (destroy@1.0.3, ms@0.7.0, mime@1.2.11)
├── accepts@1.2.2 (negotiator@0.5.0, mime-types@2.0.7)
└── type-is@1.5.5 (mime-types@2.0.7)
```
> Notice that a new folder "node_modules" will be created storing the dependency packages.
> Never commit them into git to save space. Your remote environment should download and install the dependencies by itself. So, exclude this folder from git's control by: ```$ echo "node_modules/*" >> .gitignore```
