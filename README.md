# QR Code Generator

A simple web app that turns any text or URL into a QR code. Type something, click a button, and the QR code appears instantly.

Built with plain **HTML, CSS and JavaScript**, with no frameworks or libraries.

## Features

- Generate a QR code from any text or URL
- Input validation: asks you to enter something if the field is empty
- Special characters in URLs (`&`, `?`, `#`, spaces) are handled correctly using `encodeURIComponent`
- Smooth slide-down animation when the QR code appears
- Clean, centered card layout

## Demo

<img width="1917" height="970" alt="image" src="https://github.com/user-attachments/assets/f1b44a11-6d40-428e-b63e-4205ef6a2bf4" />
<img width="1917" height="968" alt="image" src="https://github.com/user-attachments/assets/112328ac-c918-4a4c-a21f-b1ebecbec80b" />
<img width="1917" height="967" alt="image" src="https://github.com/user-attachments/assets/44d0d679-5638-445c-ae7c-26cbca7b6760" />




## Tech Stack

| Technology | Used for |
| --- | --- |
| HTML5 | Page structure |
| CSS3 | Layout, styling and animation (Flexbox, transitions) |
| JavaScript | Reading input, validation and updating the QR image |
| [QRServer API](https://goqr.me/api/) | Generating the QR code image |

## Project Structure

```
qr-code-generator/
├── index.html    # Page markup and JavaScript logic
├── style.css     # All styling
└── README.md
```

## How to Run

No installation or build step is needed.

1. Download or clone this repository:
   ```bash
   git clone https://github.com/dustrik18/qr-code-generator.git
   ```
2. Open the folder and double-click `index.html` to open it in your browser.
3. An internet connection is required, since the QR image is fetched from the API.

## How to Use

1. Type or paste any text or URL into the input box.
2. Click **Generate QR Code**.
3. Scan the QR code with your phone camera, or right-click the image to save it.

## How It Works

When you click the button, the script reads the input and sets it as part of the image URL:

```js
qrimg.src = "https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=" + encodeURIComponent(qrText.value);
```

The browser sends that request to the QRServer API, which returns a QR code image. The image is then shown inside a box that expands using a CSS `max-height` transition.

## Possible Improvements

- Add a button to download the QR code as an image
- Let the user choose the QR code size and colors
- Generate the QR code locally with a JavaScript library so it works offline

## Author

**Tanish Sahu**
GitHub: [dustrik18](https://github.com/dustrik18)
