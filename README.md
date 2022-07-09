# promptJS
A JS Library to prompt input dialogs dynamically so you don't have to waste time writing HTML

### Sypnosis

To prompt user for area of a square, normally you'd —
```javascript
  let s = window.prompt('Enter square side length:')
  console.log(`The area of the square is ${s*s}`)
```

but for rectangle this code becomes unusable, so you can use **promptJS** —
```javascript
  prompt.inputModal("Area of Rectangle",["Enter Length:","Enter Width:"], (l,b)=>{
        console.log(`Area of the rectangle is ${l*b}`)
  })
```
<p align='center'>
  <img src="https://github.com/besnoi/promptJS/blob/main/_img/preview.JPG"><br>
  <em>Output may vary depending on your Bootstrap theme</em>
</p>

### Dependencies
- *jQuery v2.1.3*
- *Bootstrap v4.0.0*

### Usage
For single/multiple input dialogs -
```javascript
prompt.inputModal(title,[label1, label2,...],
          (input1, input2,...)=>{
            //do stuff with inputs
})
```
For simple message dialogs - 
```javascript
prompt.message(title,body)
```

To call a predefined modal
```javascript
prompt.call(title)
```

### Example
```javascript
prompt.inputModal("Greetings",["What's ur name?"],function (name){
        console.log(`Well, Hello ${name}`)
})

prompt.message("About","Prompt v.1.0")

prompt.call("Greetings")
```

Consider studying [graphviz](https://github.com/besnoi/graphviz/blob/main/index.html#L30) for a project-example
### Todo 
- ~Add examples, screenshots, etc~
- Make more projects demonstrating usefulnes of promptJS
