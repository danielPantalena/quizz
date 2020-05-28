---
title: Primeira pergunta
tags:
  - set
  - object
order: 2
date: '2019-09-27'
answers:
  - 'oneObject.feito '
  - 'oneObject['valor2']'
  - 'oneObject.key2.feito // correct' 
---

Como acessar 'valor2' ?

```javascript
const oneObject = {
  chave0: 'valor0',
  chave1: 'valor1',
  key: {
    key1: 'value1'
    key2 : {
      chave : 'valor',
      feito : 'valor2'
    }
  }
};

```

<!-- explanation -->

While it's true a `Set` object will remove duplicates, the two values we create our `Set` with are references to different objects in memory, despite having identical key-value pairs. This is the same reason `{ a: 1 } === { a: 1 }` is `false`.

It should be noted if the set was created using an object variable, say `obj = { a: 1 }`, `new Set([ obj, obj ])` would have only one element, since both elements in the array reference the same object in memory.
