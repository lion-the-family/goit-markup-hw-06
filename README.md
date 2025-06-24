# Web Studio Landing Page

A responsive landing page for a fictional digital studio called **Web Studio**. This project is built with **HTML5**, **CSS3**, and includes **mobile-first responsive navigation**, **modals**, and modern UI elements.

---

## ✨ Features

- Responsive layout using CSS and [modern-normalize](https://github.com/sindresorhus/modern-normalize)
- Header with navigation and mobile menu (burger button)
- Contact information using `<address>`
- Hero section with call-to-action button
- Modal form with name, phone, email, and comment fields
- Privacy policy acceptance checkbox
- Social media links (Instagram, Twitter, Facebook, LinkedIn)
- Google Fonts integration (Raleway, Roboto)

---

## 📁 Project Structure

project/
├── index.html
├── css/
│ └── styles.css
├── js/
│ ├── modal.js
│ └── menu.js
└── images/
└── icons.svg

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open `index.html` in your browser.
3. Make sure you have an internet connection for external resources like fonts and normalize.css.

---

## 📌 Technologies Used

- HTML5 & Semantic Tags
- CSS3 (including Flexbox and Grid)
- JavaScript (for modal and mobile menu logic)
- SVG Icons
- Google Fonts
- Normalize.css (modern-normalize)

---

## 🧠 Mobile Menu Logic (`menu.js`)

This script controls the opening and closing of the mobile menu using `data-` attributes and a toggle class.

### 🔍 How It Works

```js
(() => {
  const refs = {
    openModalBtn: document.querySelector("[menu-modal-open]"),
    closeModalBtn: document.querySelector("[menu-modal-close]"),
    modal: document.querySelector("[menu-modal]"),
  };

  refs.openModalBtn.addEventListener("click", toggleModal);
  refs.closeModalBtn.addEventListener("click", toggleModal);

  function toggleModal() {
    refs.modal.classList.toggle("is-open");
  }
})();
