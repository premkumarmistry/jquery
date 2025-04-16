
# jQuery 

This project demonstrates how to use **jQuery** for dynamic web development. It covers the following key concepts:

### 1. jQuery Syntax

#### Concept:
jQuery ka basic syntax kuch is tarah hota hai:
```javascript
$(selector).action();
```
Selector ko use karke hum kisi HTML element ko select karte hain, aur action() method ko apply karte hain.

#### Example:
Agar humko kisi paragraph ke andar ka text change karna ho, to hum aise likhenge:

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  </head>
  <body>
    <p id="message">Ye pehle wala text hai.</p>
    <button id="changeTextBtn">Change Text</button>

    <script>
      $(document).ready(function() {
        $("#changeTextBtn").click(function() {
          $("#message").text("Ye naya text hai!");
        });
      });
    </script>
  </body>
</html>
```

#### Explanation:
- `$("#message")` se hum `<p>` tag ko select karte hain.
- `.text("Ye naya text hai!")` se hum uska text change kar dete hain.

### 2. jQuery Selectors

#### Concept:
Selectors ka use karke hum HTML elements ko unke tag, class, ya id ke through select karte hain.

#### Example:
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  </head>
  <body>
    <p class="highlight">Ye ek paragraph hai.</p>
    <p id="para2">Ye doosra paragraph hai.</p>
    <button id="btn">Click Me</button>

    <script>
      $(document).ready(function() {
        $("#btn").click(function() {
          $(".highlight").css("color", "red");  // Class select karke uska color red karna
          $("#para2").css("font-size", "20px");  // ID select karke font size badhana
        });
      });
    </script>
  </body>
</html>
```

#### Explanation:
- `$(".highlight")` se hum class "highlight" wale element ko select karte hain.
- `$("#para2")` se hum ID "para2" wale element ko select karte hain.

### 3. jQuery Event Methods

#### Concept:
jQuery mein events handle karna bahut asaan hota hai. Aap click, hover, focus jaise events ko easily handle kar sakte ho.

#### Example: Click Event
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  </head>
  <body>
    <button id="clickBtn">Click Me</button>

    <script>
      $(document).ready(function() {
        $("#clickBtn").click(function() {
          alert("Button clicked!");
        });
      });
    </script>
  </body>
</html>
```

#### Explanation:
- `$("#clickBtn").click()` se hum button ke click hone par ek action define karte hain.
- Jab button click hoga, ek alert show hoga.

### 4. jQuery Effects: Hide and Show

#### Concept:
jQuery mein aap easily kisi element ko hide ya show kar sakte ho using `.hide()` and `.show()`.

#### Example: Hide and Show
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  </head>
  <body>
    <div id="message">Ye ek message hai!</div>
    <button id="toggleBtn">Hide/Show</button>

    <script>
      $(document).ready(function() {
        $("#toggleBtn").click(function() {
          $("#message").toggle();  // Show/Hide element
        });
      });
    </script>
  </body>
</html>
```

#### Explanation:
- `$("#message").toggle()` se element ko hide ya show karte hain. Agar element already visible hai to hide ho jayega, aur agar hidden hai to show ho jayega.

### 5. jQuery Effects: Fading

#### Concept:
jQuery mein fading effects bhi bahut simple hote hain. Aap `.fadeIn()` aur `.fadeOut()` methods ka use karke elements ko smoothly hide/show kar sakte ho.

#### Example: Fade In/Out
```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  </head>
  <body>
    <div id="message" style="display:none;">Ye message fade ho raha hai!</div>
    <button id="fadeBtn">Fade In/Out</button>

    <script>
      $(document).ready(function() {
        $("#fadeBtn").click(function() {
          $("#message").fadeIn();  // Fade in element
        });
      });
    </script>
  </body>
</html>
```

#### Explanation:
- `$("#message").fadeIn()` se element dhire-dhire appear hota hai.
- Agar aap `.fadeOut()` use karenge to element dhire-dhire disappear ho jayega.

---

### **Summary of Key Concepts:**
- **jQuery Syntax**: Simpler syntax to select and apply actions to elements.
- **Selectors**: Select elements using ID, class, or tag.
- **Event Methods**: Handle events like click, hover, etc. easily.
- **Effects (Hide/Show)**: Easily toggle visibility of elements.
- **Fading**: Smooth transitions to hide or show elements.

