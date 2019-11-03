# range-en-javascript
funcion range() en javascript...

## Construida con bucle for
```javascript
function range(start, end) {
    let ans = [];
    for (let i = start; i <= end; i++) {
        ans.push(i);
    }
    return ans;
}
```
## Solucion recursiva
```javascript
function range(start, end) {
    if(start === end) return [start];
    return [start, ...range(start + 1, end)];
}
```
## Utilizando new Array()
```javascript
function range(start, end) {
    return (new Array(end - start + 1)).fill(undefined).map((_, i) => i + start);
}
```
## Usando generadores
```javascript
function* range(start, end) {
    for (let i = start; i <= end; i++) {
        yield i;
    }
}
```
```javascript
function* range(start, end) {
    yield start;
    if (start === end) return;
    yield* range(start + 1, end);
}
```
Uso:
```javascript
for (i of range(1, 5)) {
    console.log(i);
}

[...range(1, 5)]
```
## Ninja range
```javascript
let range = (s, e) => Array.from('x'.repeat(e - s), (_, i) => s + i);
```

## Bucle for, forEach, for in, for of 
La mayoria de estas funciones construidas se pueden usar con cualquiera de estos bucles, dependera del uso para seleccionar la opcion mas adecuada.

```javascript
range(0,5).forEach(element => {
    console.log(element);
});
```