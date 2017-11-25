## on Mainpage
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <div id="weather"></div>
    <script src="../node_modules/steal/steal.js" main="@empty"></script>
    <script type="text/steal-module">
      import weather from "myhub/weather/weather";
      weather("#weather");
    </script>
  </body>
</html>
```

## as import able webcomponent with auto registering tag inserted already in import owner

main.html
```html
<!-- In Production can also be simply the path to your Steal.production.js you should if you want to use components never bundle steal -->
<script src="/node_modules/steal/steal.js" main="@empty"></script>
<link rel="import" src="import.html">
```

import.html
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    <script src="/node_modules/steal/steal.js" main="@empty"></script>
    <script type="text/steal-module">
      import weather from "myhub/weather/weather";
    </script>
  </body>
</html>
```
