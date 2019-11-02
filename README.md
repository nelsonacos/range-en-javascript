# range-en-javascript
funcion range() en javascript...

```javascript
function range(start, end) {
    if (end - start === 2) {
        return [start + 1]
    } else {
        let list = range(start, end -1);
        list.push(end - 1);
        return list
    }
    
}
```

su uso:

```javascript
range(0,9).forEach(element => {
    console.log(element);
});
```
