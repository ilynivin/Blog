---
title: "Create Cli Portfoilo"
subtitle: "Create A CLI Game In Simple Steps"
date: 2023-05-01T12:09:09+05:30
draft: false
tags: ["CLI"]
---

# Create A Cli Game 

To create a cli game follow my steps

---

### ✏️ <ins>Step 1:</ins>

Create a folder and Name it What ever you want and install the following Packages in the folder using Command Prompt in your terminal 

```
npm i chalk
npm i chalk-animation
npm i figlet
npm i gradient-string
```

*Note*:*Install [Node.js](https://nodejs.org/en) in your System*


### ✏️ <ins>Step 2:</ins>

Create a file called `index.js` In your folder and Write some code 

In `index.js` Import all the pakages by pasting the following Code and Also include the SHEBANG
```
#!/usr/bin/env node

// SHEBANG 👆 (#!)

// Import 
import chalk from "chalk";
import figlet from "figlet";
import gradient from "gradient-string";
import chalkAnimation from "chalk-animation";
```
### ✏️ <ins>Step 3:</ins>

Type your code. In this blog i will give a Sample Code 

```
let playername; 

// Timer to stop the animation 👇

const sleep = (ms = 2000) => new Promise((r) => setTimeout(r,ms))



// Function 1 ( Welcome ) 👇
async function Welcome(){

    const rainbowTitile = chalkAnimation.rainbow('Welcome to My Profile \n');
    await sleep();
    rainbowTitile.stop();
}

// Function 2 (About me ) 👇

async function Aboutme(){

    const rainbowTitile  = chalkAnimation.neon('About Me \n')
    await sleep();
    rainbowTitile.stop();

    console.log(`
    Hai I am ${chalk.bgBlue('Nivin')}. A 15 y/o Web devaloper and App devaloper 
    I have started my Coding journey since is was at ${chalk.bgGrey('6th')}.
    I am Living under the city Working to Make ${chalk.bgGreen('Cool Stuffs')}.
    In my spare time i have create 15+ Repo in my ${chalk.bgCyanBright('Github ')}.
    I am a huge fan of ${chalk.bgYellow('Robotics')} and i have create a Robotics since i was at 5th.

    `);
}


// Function 3 (Skills ) 👇
async function skills(){

    const rainbowtitile = chalkAnimation.pulse('Skills \n')
    await sleep();
    rainbowtitile.stop();

    console.log(`
    ${chalk.bgYellow('Java Script')}
    ${chalk.bgRed('HTML')}
    ${chalk.bgBlue('Css')}
    ${chalk.bgGreen('Python')}
    ${chalk.bgGray('MarkDown')}

    `)
}


// Function 4 (Projets ) 👇
async function projets(){

    const rainbowtitile = chalkAnimation.karaoke('My Projects \n')
    await sleep();
    rainbowtitile.stop();

    console.log(`
    
    ${chalk.bgMagenta('My Portfolio Website')}
    ${chalk.bgBlueBright('My Blog')}
    ${chalk.bgGreen('Js Counter')}
    ${chalk.bgCyanBright('Calculator')}
    `)

}


// Function 5 (ASCII Display ) 👇
 async function End(){
        const msg = `Thank you for Reading `
    
        figlet(msg, (err , data) => {
            console.log(gradient.pastel.multiline(data));
        });
    }



// Order of the Program to Run 👇

await Welcome();
await Aboutme();
await skills();
await projets();
await End();

```

### ✏️ <ins>Step 4:</ins>

In your `package.json` add this command ` "type": "module"` and `"bin": "./index.js"`


### ✏️ <ins>Step 5:</ins>

To Run the Program type in your Command Prompt `node .`.

And thats all This is how you can create . 

Hope you like this Post 💖