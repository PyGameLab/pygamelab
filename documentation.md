# Documentation page

## 1. Console functions
- Get the console functions: `from PyGameLab import console`
</br>

- `console.log(*text, sep=" ")`
  - Similar to `print()`
  - Usage: `console.log("Hello,", "world!")` Prints `Hello, world!` to console.
</br>

- `console.warn(*text, sep=" ")`
  - Prints yellow text to console, indicating that there is a warning.
  - Usage: `console.warn("Warning", "message.")` will print `Warning message.` in yellow.
</br>

- `console.error(*text, sep=" ")`
  - Prints a red text to console, indicating that there's a problem.
  - Usage: `console.error("Line 101:", "Error message")` This will print `Line 101: Error message` in red.

## 2. Data handling
- Get the PyGameLab data: `from PyGameLab import data`
</br>

- `dependences`:
  - List of all modules the project is using. Useful to install missing requirments.
</br>

- `initialized`:
  - If the line `pygamelab.init()` was in the code, this should be `True`.
 </br>
 
- `version`:
  - The current version of PyGameLab
 </br>
 
- `interpreter`:
  - The interpreter I was using when I did the library
 </br></br>
 
## 3. Colors usage
- Get the colors from PyGameLab: `from PyGameLab import colors`

- `text`:
  - The color codes for text.
  - Structure: `text.C{num}` where `num` can be a number from 0 to 255.
  - Reset: `text.RESET` resets the color to the default one.
  - Usage: `print(text.C1, "Hello, world", text.RESET, sep="")` Prints a red text saying `Hello, world` to the console.
</br>

- `background`:
  - The color code for text background.
  - Structure: `background.C{num}` where `num` can be a number from 0 to 255.
  - Reset: `background.RESET` resets the color to the default stage.
  - Usage: `print(background.C255, "Hello, world", background.RESET, sep="")` Prints text `Hello, world` in a white background.
 </br>
 
- `styles`:
  - `RESET_ALL`: Resets all styles (background, text).
  - `BRIGHT`: Makes the actual color (background and text) brighter.
  - `DIM`: Makes the actual color (background and text) darker.
  - `ITALIC`: Makes the text italic.
  - `UNDERLINE`: Underlines the text.
  - `BLINK`: Make the text to blink.
  - `REVERSE`: Reverses the text.
  - `HIDDEN`: Hides the text.
  - Usage: `styles.{style_name} + text
</br></br>

## 4. Date usage
- Get the date information: `from PyGameLab import date`
</br>

- variables:
  - `today`: The today information in yy/mm/dd
  - `now`: The today information and time. Format: yy/mm/dd h-m-s.ms
  - `time`: The time information in h-m-s.ms
  - `second`: The seconds of time
  - `minute`: Minutes of time
  - `hour`: Hours of time
  - `year`: Years of today
  - `day.number`: number of day of today
  - `day.name`: name of the day in week
  - `month.number`: Number of the month
  - `month.name`: name of the month
 </br></br>

 ## 5. Unicode characters
 - Start unicode module:
```Python
from PyGameLab import unicode
unicode.init()
```
</br>

- Get a character:
  - Get the unicode list after using `unicode.init()` with `Unicode.unicode`.
  - Get a unicode character by its name: `unicode.char(name)`
</br>

## 6. Random functions
- Get the functions: `from PyGameLab import random`
</br>

- `random.integer(a, b)` returns a random integer between a and b
- `random.float(a, b)` returns a random floating number between a and b
- `random.choice(seq)` returns a random item from list sequence `seq`
- `random.letter()` returns a random letter
- `random.boolean()` returns a random boolean (True or False)
- `random.element(string)` returns a random character from a string
- `random.sample(lst, k)` returns a random sample from a list starting from k
- `random.shuffle(lst)` returns the given list shuffled
- `random.color()` return a random rgb color
- `random.code(lenght, uppercase=True, lowercase=True, rep=True)` returns a random code of a given lenght. You can chose wether if uppercases or lowercases are. You can also admit repeated digits (rep)
- `random.password(length, uppercase=True, lowercase=True, numbers=True, special_chars=True) returns a random password of the selected lenght. You can customize it using the parameters
</br>

## 7. Storage manipulation
- Get the storage functions: `from PyGameLab import storage`
</br>

- `storage.read(file_path)` returns the content of a file from the given file path
- `storage.write(content, file_path)` writes a new content/file on the given file path
- `storage.append(content, file_path)` appends content at the end of a file on the given file path
- `storage.JSON`:
  - `storage.JSON.read(file_path, data_path)` reads the content of a json file on the given file path. It can also read data from inside the json file
  - `storage.JSON.exists(file_path)` returns True if the given file on the file path exists
  - `storage.JSON.write(file_path, data)` writes a new json content/file on the given file path
</br>

## 8. Constant variables usage
- Get the constants: `from PyGameLab import constants`
</br>
The constants writed there, are to use the `alignments` and `mouse_buttons` on other parts of code.
</br>

## 9. Screen usage
- Get the Window class: `from PyGameLab import Window`
</br>

- The Window class is a simplified way to create multiple windows at once.
- Create a new Window instance:
```Python
from PyGameLab import Window
myScreen = Window(
  size = (100, 100),
  caption = "[Window Title Here]",
  color = (255, 255, 255)
)
while myScreen.running:
  myScreen.update()
pygame.quit()
```
- This piece of code, imports the class Window from PyGameLab and creates a new instance for `myScreen`, of `Window`, taking as parameters a tupple of the size (w, h), a caption and a background color in RGB.
- You can also get the screen information using `myScreen.height`, `myScreen.width`, `myScreen.caption` and `myScreen.backgroundColor`
- Again in the code, the same uses `myScreen.running` to check if the actual Window `myScreen` is still on.
- It also uses `myScreen.update()`, this is useful when we edit a value of the current Window.
- Finally, it uses `pygame.quit()` to end the screen.

## 10. Displaying text on screen
- Get the Window and Text class: `from PyGameLab import Window, Text`
</br>

- Display text:
  - Structure:
    ```Python
    Text.display(screen, text, position, color, font, size, alignment)
    ```
  </br>
  
  - Usage:
    - `screen` is a variable name of type Window
    - `text` is a string. The text that will be showed on screen
    - `position` tupple. Structure: `(x, y)`
    - `color` is the rgba color that the text will have
    - `font` the font of the text
    - `size` the size of the text
    - `alignment` the alignment of the text. Tupple. Structure: `(horizontal, vertical)`. Try using the constants variables.
 </br>
 
  - Eg:
    ```Python
    from PyGameLab import Window, Text

    screen = Window((100, 100), "Text test", (255, 255, 255))
    text = Text.display(screen, "Hello, World", (50, 50), (0, 0, 0, 255), None, 10, constants.MIDDLECENTER)

    while screen.running:
      screen.update()
      text = Text.display(screen, "Hello, World", (50, 50), (0, 0, 0, 255), None, 10, constants.MIDDLECENTER)
    ```
  </br>
  
- Delete text:
    - Structure:
      ```Python
      
