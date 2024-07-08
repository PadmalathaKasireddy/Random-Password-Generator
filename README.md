# Random Password Generator

## Description
This is a Random Password Generator web application. It allows users to specify the length of the password and generates a random password containing alphanumeric characters and special symbols.

## Features
- Specify the length of the password.
- Generate random passwords with a mix of alphanumeric characters and special symbols.
- Simple and user-friendly interface.

## Technologies Used
- HTML
- CSS
- JavaScript
- Bootstrap 5

## How to Use
1. Clone the repository to your local machine.
    ```bash
    git clone https://github.com/your-username/random-password-generator.git
    ```
2. Navigate to the project directory.
    ```bash
    cd random-password-generator
    ```
3. Open `index.html` in your preferred web browser.

## File Structure

random-password-generator/
│
├── index.html
├── style.css
└── script.js

```less

- `index.html`: The main HTML file containing the structure of the web page.
- `style.css`: The CSS file for styling the web page.
- `script.js`: The JavaScript file containing the logic for generating the random password.

## Code Overview

### HTML
The HTML file contains a form for inputting the password length and a button to generate the password. It also displays the generated password.

### CSS
The CSS file includes styles for the container, card, input fields, and buttons.

### JavaScript
The JavaScript file contains functions to generate a random password based on the specified length and character set.

```javascript
document.getElementById('generate-button').addEventListener('click', function() {
    var length = document.getElementById('password-length').value;
    var password = generatePassword(length);
    document.getElementById('generated-password').value = password;
});

function generatePassword(length) {
    var charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()_-+=<>?/{}[]|";
    var password = "";
    for (var i = 0; i < length; i++) {
        var randomIndex = Math.floor(Math.random() * charset.length);
        password += charset[randomIndex];
    }
    return password;
}
```

