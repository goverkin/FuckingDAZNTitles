# FuckingDAZNTitles
Copy and paste this script to your browser console to remove DAZN YouTube videos title and thumbnail:

```
var elements = document.getElementsByClassName("style-scope ytd-thumbnail")
for (let i = 0; i < elements.length; i++) {
  elements[i].innerHTML = '';
}

var elements = document.querySelectorAll('[id=video-title]')
for (let i = 0; i < elements.length; i++) {
  let text = elements[i].innerHTML;
  const myArray = text.split("|");
  elements[i].innerHTML = myArray[1];
}
```
