---
title: "Codigo Vue"
date: 2020-08-06T14:19:38-05:00
draft: false
---

``` html
<!doctype html>
<html>
<head>
  <title>Prueba Vue</title> 
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
</head>
<body>
  <div id="aplicacion">{{mensaje}}</div>
  
  <script src="https://cdn.jsdelivr.net/npm/vue"></script>   

  <script>
  var app = new Vue({
    el:'#aplicacion',
    data:{
      mensaje: 'hola mundo Vue'
    }
  })
</script>
</body>
</html>

```
