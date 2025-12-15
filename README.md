# ✈️ Air Message

## Project Name: Air Message

A whimsical web application that transforms user-inputted text into animated, pixel-art banners trailed behind a squadron of flying airplanes. It is a creative way to display a message with a retro, sprite-based aesthetic.

## ✨ Features

* **Animated Airplanes:** Uses SVG pixel art for the airplane sprites, featuring random color schemes.
* **Bouncing/Bobbing Movement:** The airplanes and the attached message modules (`.module` elements) have a subtle, continuous up-and-down "bop" animation.
* **Dynamic Message Banners:** The user's message is split into words (or sections) and distributed among multiple planes. The application interprets a space (' ') in the input as the divider between words/modules.
* **Responsive Banner Logic:** The JavaScript dynamically calculates word wrapping using "ghost" elements (`.message_ghost`) to determine how to split the message across different planes based on the current viewport width (`calcWrapIndex`, `splitTextForBanners`).
* **CSS-only Animation:** The core flying movement is achieved by transitioning the plane's `left` CSS property.

## 🛠️ Technology Stack

* **HTML:** For the structure (`air messge.html`).
* **CSS:** For styling and visual layout (`style.css`).
* **JavaScript (Vanilla JS):** For application logic, SVG rendering, animation control, and responsive text splitting (`script.js`).
* **SVG:** Used to define the pixel-art airplane and rope sprites.
* **Font:** Uses the 'Press Start 2P' font for a retro look.

## 🚀 Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/kunalhacker22/Air-Message.git]
    ```
2.  **Open the File:**
    Open the `air messge.html` file directly in your web browser.

### Usage

1.  **Enter your Message:** Type your message into the text area at the bottom of the screen. The script replaces spaces with '#' internally to process the text (`bannerContent = textarea.value.replaceAll('#','&num;').replaceAll(' ','#')`).
2.  **Create Banners:** Click the **`create`** button to launch the planes.

## ⚙️ Key Functionality (From `script.js`)

| Function | Purpose |
| :--- | :--- |
| `planeSvg()` | Renders a random-colored pixel-art airplane SVG. |
| `bop()` | Implements the continuous, oscillating up-and-down movement for planes and messages. |
| `calcWrapIndex()` | Determines the line break points for the message based on current screen size using temporary, hidden "ghost" elements. |
| `splitTextForBanners()` | Uses the wrap index to divide the full user message into separate parts (`banners`), with each part assigned to a different plane. |
| `createPlane()` | Renders a single plane and its attached message modules, sets its starting position (`left: 100%`), and initiates its flight path (`plane.style.transition = '6s ease'`). |
| `resetPlanes()` | Clears all existing timers and planes, recalculates the banners based on the current window size and message, and restarts the plane launch sequence. |

## 📸 Screenshots

*(Add a screenshot or GIF of your project running here)*
