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

Right click on the page once you are inside the DAZN channel and click on `Inspect` to open the browser console.<br />
Copy and paste the code inside the console and hit enter.<br />
The first part of the code removes the thumbnails and the second part removes the revealing part of titles (before `|`)<br />
