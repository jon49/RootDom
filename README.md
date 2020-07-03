# RootDom

E.g.,

```js
test = 
   new RootEl(
      ['div', {id: 'write2'}, [
         ['h1', {text: "Orange2!", update: {title: ['text', 'title']}}],
         ['p', {update: {title: ['text']}}],
         ['a', {update: {yep: ['text'], url: ['href']}}]
      ]])
document.body.appendChild(test.el)
```

To update:

```js
test.update({title: "Yellow!", yep: "OK", url: "https://example.com"})
```

Note that you do not need to have all the different values, you can update with just a
partial object and those will not be updated. To remove a value set the value to `null`
or `undefined`:

```js
test.update({title: undefined})
```
