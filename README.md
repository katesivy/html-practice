# html-practice
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <title>Meta examples</title>
    
    <meta name="author" content="Chris Mills">
    <meta name="description" content="This is an example page to demonstrate usage of metadata on web pages.">

    <meta property="og:image" content="https://developer.cdn.mozilla.net/static/img/opengraph-logo.dc4e08e2f6af.png">
    <meta property="og:description" content="This is an example page to demonstrate usage of metadata on web pages.">
    <meta property="og:title" content="Metadata; The HTML &lt;head&gt;, on MDN">

    <link rel="Shortcut Icon" href="favicon.ico" type="image/x-icon">
  </head>
  <body>
    <h1>Meta examples</h1>

    <p>Japanese example: ご飯が熱い。</p>
  </body>
</html>

  
    
html {
  background-color: green;
  font-size: 20px;
}

ul {
  background: red;
  padding: 10px;
  border: 1px solid black;
}

li {
  margin-left: 20px;
}


var list = document.createElement('ul');
var info = document.createElement('p');
var html = document.querySelector('html');

info.textContent = 'Below is a dynamic list. Click anywhere outside the list to add a new list item. Click an existing list item to change its text to something else.';

document.body.appendChild(info);
document.body.appendChild(list);

html.onclick = function() {
  var listItem = document.createElement('li');
  var listContent = prompt('What content do you want the list item to have?');
  listItem.textContent = listContent;
  list.appendChild(listItem);

  listItem.onclick = function(e) {
    e.stopPropagation();
    var listContent = prompt('Enter new content for your list item');
    this.textContent = listContent;
  }
}

var list = document.createElement('ul');
var info = document.createElement('p');
var html = document.querySelector('html');

info.textContent = 'Below is a dynamic list. Click anywhere outside the list to add a new list item. Click an existing list item to change its text to something else.';

document.body.appendChild(info);
document.body.appendChild(list);

html.onclick = function() {
  var listItem = document.createElement('li');
  var listContent = prompt('What content do you want the list item to have?');
  listItem.textContent = listContent;
  list.appendChild(listItem);
