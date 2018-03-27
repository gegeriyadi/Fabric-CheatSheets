### Move Object with Keyboard

```javascript
document.onkeydown = function(e) {
switch (e.keyCode) {
  case 38:  /* Up arrow */
      if(canvas.getActiveObject()){
        canvas.getActiveObject().top -= 5;
        canvas.renderAll();
      }
    break;
  case 40:  /* Down arrow  */
      if(canvas.getActiveObject()){
        canvas.getActiveObject().top += 5;
        canvas.renderAll(); 
      }
    break;
  case 37:  /* Left arrow  */
      if(canvas.getActiveObject()){
        canvas.getActiveObject().left -= 5; 
        canvas.renderAll();
      }
    break;
  case 39:  /* Right arrow  */
      if(canvas.getActiveObject()){
        canvas.getActiveObject().left += 5; 
        canvas.renderAll();
      }
    break;
  case 46:  /* delete */
      if(canvas.getActiveObject()){
        var obj = canvas.getActiveObject(); 
		canvas.remove(obj);
      }
    break;

}}
```
