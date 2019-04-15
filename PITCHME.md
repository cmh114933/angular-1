## Week 3: Angular 1

---

Run this command in powershell

```bash
npm install -g @angular/cli

# when prompted, select no routing, CSS
ng new tic-tac-toe
```

* you may need to connect to Dell Guest Network

---

### HTML/JS

- write content using HTML
- add events using JS
- change HTML/CSS when JS events are triggered

+++

### JS Web Frameworks

- JS generates HTML
- events cause variables to change
- variable changes cause HTML to be regenerated

---

### Tic Tac Toe

+++

- click cell to place 'X', 'O' piece
- hover over occupied cell, set bg color to red
- hover over empty cell, set bg color to green

+++

### HTML/JS Approach

- create cells in HTML
- when click, set 'X' / 'O' innerHTML
- when hover, check innerHTML and set bg color

+++

### Web Framework Approach

- what is the state of the game
    - what moves have already been played
    - which cell is currently being hovered over
- for each cell
    - if move played in current cell, place piece
    - if `cellIndex === hoveredOverIndex`
        - check if move played in current cell
        - set bg Color

---

### Intro To Angular

---

```bash
# creates new Angular project
ng new <app-name>

# run Angular server
ng serve
ng serve --port <number 4000>
```

+++

### Angular Components

- Typescript file
    - contains functions/events/logic
- HTMl file
    - contains displayed HTML
- CSS file
    - contains styling
- Typescript Spec file
    - contains tests (ignore for now)

---

### Typescript -> HTML Variables

```ts
// app.component.ts
class AppComponent {
    var1: number = 123
    var2: string = "abc"
}
```

```html
<!-- app.component.html -->
<div>{{ var1 }}</div>
<div>{{ var2 }}</div>
```

```html
<!-- rendered html -->
<div>123</div>
<div>abc</div>
```

+++

### If / Else in HTML

```html
<div *ngIf="var1 > 5">
    It's huge!
</div>
<div *ngIf="var1 < 5">
    It's small!
</div>
```

+++

### For Loop in HTML

```html
<div *ngFor="let move of moves">
    <div class="cell">{{move}}</div>
</div>
```

```html
<div *ngFor="let move of moves; let i = index">
    <div class="cell">{{i}}. {{move}}</div>
</div>
```







