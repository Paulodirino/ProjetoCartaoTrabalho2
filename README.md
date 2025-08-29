# Interactive Credit Card Project (Android)

## Summary

This is an Android project developed in Android Studio that simulates an interactive credit card interface. The main goal is to demonstrate skills in XML layout design, UI manipulation with Kotlin, implementation of real-time field formatting, input validations, and basic animations.

## Implemented Features

*   **Dynamic Card Visualization:** Data entered into the form fields is reflected in real-time on the visual representation of the credit card.
*   **Card Front and Back:** The card has a front and a back view.
*   **Flip Animation:** Clicking on the card triggers a "flip" animation, toggling between the front and back views.
*   **Automatic Field Formatting:**
    *   **Card Number:** Automatically formatted with spaces every four digits (e.g., `1234 5678 9101 1213`).
    *   **Expiry Date:** Automatically formatted to the `MM/YY` standard.
*   **Real-time Field Validation:**
    *   **Cardholder Name:** Must contain at least 3 characters.
    *   **Card Number:** Must contain exactly 16 numeric digits.
    *   **Expiry Date:** Must follow the `MM/YY` format and be a valid date (not expired and month between 01-12).
    *   **CVV:** Must contain exactly 3 numeric digits.
    *   Error messages are displayed directly in the fields if validation fails.
*   **Custom Layout:**
    *   Use of `CardView` to give the appearance of a real card with rounded corners and shadow.
    *   Icons to represent the chip and card brand (Visa, in this example).
    *   Styled input fields (`EditText`) and display fields (`TextView`).

## Code Structure

*   **`MainActivity.kt`**: The main Activity that manages all the user interface logic, including:
    *   View initialization.
    *   Configuration of `TextWatcher`s for real-time formatting and validation.
    *   Implementation of the card flip animation.
    *   Updating the visual card's `TextView`s.
*   **`activity_main.xml`**: The layout file that defines the visual structure of the screen, containing:
    *   The main `CardView` enveloping the card's front and back.
    *   Separate layouts for the front (`cardFrontLayout`) and back (`cardBackLayout`).
    *   `EditText`s for user data input (card number, name, expiry, CVV).
    *   `TextView`s to display the formatted data on the visual card.
*   **Drawables**:
    *   `card_background.xml`: Defines the background style for the card's front.
    *   `card_background_back.xml`: Defines the background style for the card's back.
    *   Vector icons (e.g., `ic_chip.xml`, `ic_visa.xml`).

## How to Compile and Use

1.  Clone the repository or import the project into Android Studio.
2.  Compile and run the application on an Android emulator or physical device.
3.  Interact with the form fields:
    *   Enter the cardholder's name.
    *   Insert the card number.
    *   Provide the expiry date.
    *   Enter the CVV.
4.  Observe the real-time formatting and validations.
5.  Click on the card to see it flip and display the opposite side.

## Screenshots

**Example of how to add in Markdown:**
```markdown
### Card Front
![Frente](https://github.com/user-attachments/assets/bed06e52-6c7f-4746-b471-3a636755fcdc)


### Card Back
![Fundo](https://github.com/user-attachments/assets/6132ca1a-5fa2-42f7-a0a0-aafe13eff8b3)


```

## Potential Future Improvements

*   Automatic detection of the card brand based on the number.
*   More elaborate animations.
*   Light and dark themes.
*   Integration with more robust validation libraries.
