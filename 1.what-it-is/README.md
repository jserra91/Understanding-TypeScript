# 1. Install

Install Nodejs and Typescript global module

https://nodejs.org/en/

When you finished installation, execute the next command in your command line

```
  npm install -g typescript
```

I recommended using de IDE Visual Studio Code to realize this course.

# 2. What it is typescript?

Typescript is a wrapper by Javascript.

# 3. Using Typescript (similar Hello world)

(this example is in the '1. hello world' folder)

Create folder and then create the index.html and script.ts.

In the html copy and paste the next code:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>Page Title</title>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="stylesheet" type="text/css" media="screen" href="main.css" />
    <script src="./script.js"></script>
  </head>
  <body></body>
</html>
```

After go to https://www.typescriptlang.org/play/index.html and copy and paste the example code in script.ts.

In my case...

```ts
class Greeter {
  greeting: string;
  constructor(message: string) {
    this.greeting = message;
  }
  greet() {
    return "Hello, " + this.greeting;
  }
}

let greeter = new Greeter("world");

let button = document.createElement("button");
button.textContent = "Say Hello";
button.onclick = function() {
  alert(greeter.greet());
};

document.body.appendChild(button);
```

Then compiling the typescript code with command line.

```
tsc script.ts
```

You can see the result in the folder. You should a new file called script.js.

And open the index.html with your browser.

# 4. Create a Typescript project

(this example is in the '2. my first project' folder)

Create a new npm project with this commnand

```
npm init
```

You can see a new file called package.json. Then, install the lite-server.

```
npm i lite-server --save-dev
```

then edit in package.json this line in the script

```
...
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "lite-server"
  },
...
```

then create the typescript config with this next command:

```
tsc --init
```

You can see a new file called tsconfig.json. Then execute server with this command:

```
npm run start
```

And open your browser with rute http://localhost:3000
