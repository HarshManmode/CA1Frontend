<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>3 Column Layout</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <h1>Header</h1>
  </header>

  <div class="container">
    <div class="column left">
      <p>Left Column</p>
    </div>
    <div class="column center">
      <p>Center Column</p>
    </div>
    <div class="column right">
      <p>Right Column</p>
    </div>
  </div>

  <footer>
    <p>Footer</p>
  </footer>

</body>
</html>


* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html, body {
  height: 100%;
  font-family: Arial, sans-serif;
}


header, footer {
  width: 100%;
  height: 10%;
  background-color: #333;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}


.container {
  display: flex;
  height: 80%; 
}


.left {
  width: 20%;
  background-color: darkblue;
  padding: 20px;
}


.center {
  width: 60%;
  background-color:blueviolet;
  padding: 20px;
}


.right {
  width: 20%;
  background-color:blue;
  padding: 20px;
}
