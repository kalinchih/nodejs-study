# nodejs-study

## Download Node.js

1. Download Node.js from https://nodejs.org/en/
2. Install it
3. Check the Node.js & npm version
   ```
   node -v
   npm - v
   ```

## Init a Project

1. Create a project folder (01_hello)
2. Terminal to the project folder and run the command to create a project.json file
   ```
   npm init
   ```
   Remind the entry point file name. for example, 'index.js' which is entry file to start a server server.

## Create Node.js Entry Point Fle

1. Go to project folder to create a file (index.js)
2. Go to https://nodejs.org/en/about/
3. Copy the 'hello world' codes and paste it on the index.js

```
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

## Start Hello World Server

1.  Run the command to start the Node.js server

    ```
    node index.js
    ```

    or

    ```
    npm start
    ```

    If npm ERR! missing script: start, add 'start script' in package.json

    ```
    {
        "name": "01_hello",
        "version": "1.0.0",
        "description": "",
        "main": "index.js",
        "scripts": {
            "test": "echo \"Error: no test specified\" && exit 1",
            "start": "node index.js"
        },
        "author": "",
        "license": "ISC"
    }
    ```

2.  Open http://127.0.0.1:3000/ on browser
