## What I learned in Week 8

### Monday 

Midterm

**For of loop**
An easier to write loop that can be use in many of the cases as a normal `for` loop

const colors = ['orange', 'blue', 'red', 'green', 'yellow'];

```javascript 
//for loop
for (let i=0; i<colors.length, i++) {
    const color = colors[i];
    console.log(color);
}
// for of loop
for ( const color of colors){
    if (color.length >4) {
        console.log(color);
    }
}

```

**Functions as values**

Functions can be used just like variables in code and be called upon inside other functions.

```javascript
//Example
const colors = ['orange', 'blue', 'red', 'green', 'yellow'];

for (let i = 0; i < colors.length; i++) {
  const color = colors[i];
  console.log(color);
}

for (const color of colors) {
  console.log(color);
}

//Another Example

const hello = function() {
  return 'hiiii'
}

const goodbye = function() {
  return 'bye now'
}


function callMe(func) {
  console.log(func());
}

callMe(goodbye)
callMe(hello)

```

Event listeners-
These are ways to effect the DOM based off of actions done on the HTML like clicking an image.  Allows functions to remain dormant until a specific action.

Examples-
```javascript
    function redBorder(event) {
        event.target.style.border = '5px solid red';
    }

    document.querySelector('#triceratops').addEventListener('click', redBorder)

//Example where an action effects another segment of the document

function changeBackgroundColor() {
    const findRow = document.querySelector('#row');
    let bgColor = findRow.style.background

    if(bgColor === 'red') {
        findRow.style.background = 'white';
    } else {
        findRow.style.background = 'red';
    }
}

document.querySelector('#toggle').addEventListener('click', changeBackgroundColor)

```


