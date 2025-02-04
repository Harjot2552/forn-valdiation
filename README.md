# Form Validator Webpage 📄

This project is a **Form Validator Webpage** that allows users to input their details, such as name, phone number, email, and message, with real-time validation feedback. The form ensures that all fields meet specific validation criteria before submission, improving user input quality.

## 🌐 Live Demo
Experience the form validator by opening the project in your local browser.

## 📝 Features
- **Real-time Validation:** Provides instant feedback on user input.
- **Error Messages:** Displays customized error messages for incorrect inputs.
- **Validation Indicators:** Shows a check icon (✔️) for valid fields.
- **User-Friendly Design:** Clean and simple UI for a seamless user experience.

## 🔧 Tech Stack
- **HTML**: Form structure and layout.
- **CSS**: Styling for the form and error messages.
- **JavaScript**: Form validation logic and dynamic user feedback.

## 📊 Form Validation Rules
1. **Name:**
   - Required.
   - Must contain first and last name.
   - Only alphabet characters and a single space allowed.

2. **Phone Number:**
   - Required.
   - Must be exactly 10 digits.
   - Only numeric input allowed.

3. **Email:**
   - Required.
   - Must be in valid email format (e.g., `example@mail.com`).

4. **Message:**
   - Minimum of 30 characters required.

5. **Submit Validation:**
   - All fields must pass validation for the form to be successfully submitted.

## 🔧 How It Works
- Users input data into the form fields.
- JavaScript functions validate input data and show appropriate error messages.
- Green check icons appear for valid inputs.
- If errors exist, a "Please fix the errors" message displays on form submission.

## 🔗 Setup Instructions
1. Clone the repository or download the project files.
2. Open `index.html` in your preferred browser.

## 💡 Usage
1. Enter your full name, phone number, email, and message.
2. Ensure each field turns green with the checkmark (✔️) indicator.
3. Click "Submit" to see validation in action.

## 🎨 Code Overview
### HTML
Provides the form structure and integrates icons for validation status.
```html
<div class="input-group">
    <label>Email Id</label>
    <input type="email" placeholder=" Email" id="contact-email" onkeyup="validateEmail();">
    <span id="email-error"></span>
</div>
```

### JavaScript
Implements validation functions for all form fields.
```javascript
function validateEmail() {
    var email = document.getElementById('contact-email').value;

    if (email.length == 0) {
        emailError.innerHTML = 'Email is required';
        return false;
    }
    if (!email.match(/^[A-Za-z\._\-[0-9]*[@][A-Za-z]*[\.][a-z]{2,4}$/)) {
        emailError.innerHTML = 'Email is invalid';
        return false;
    }

    emailError.innerHTML = '<i class="fa-solid fa-circle-check"></i>';
    return true;
}
```

### CSS
Handles styling for input groups and error messages.
```css
.input-group span {
    color: red;
}
```

## 📝 Possible Enhancements
- Add server-side validation for increased security.
- Style improvements using modern frameworks (e.g., Bootstrap or Tailwind CSS).
- Display success messages after form submission.

## 🚀 Conclusion
This form validator project demonstrates how to enhance user experience through real-time input validation using vanilla JavaScript. Happy coding! 😍

