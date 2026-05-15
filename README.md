# Smart Watch Component Atlas

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Status](https://img.shields.io/badge/status-live-brightgreen)

> **An interactive reference website detailing every critical component inside modern smartwatches** — from SoCs and sensors to batteries and connectivity modules.

🔗 **Live Demo:** [View the Smart Watch Component Atlas](#) *(replace with your GitHub Pages or hosting link)*

---

##  Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [Component Database](#component-database)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Customization](#customization)
- [Technologies Used](#technologies-used)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

##  About the Project

The **Smart Watch Component Atlas** is a single‑page educational web application that showcases the hardware powering today's wearables (Apple Watch, Samsung Galaxy, Garmin, etc.). It presents **12 core components** with real‑world specifications, organized into five categories:

- **Core & Memory** – SoC, RAM, Storage  
- **Display & Input** – AMOLED, Haptics, Crown  
- **Sensors** – HRM, ECG, IMU, Temperature  
- **Power** – Li‑Po Battery, Wireless Charging  
- **Connectivity** – GPS, Bluetooth, Wi‑Fi, NFC  

Each component is displayed on an interactive card with technical details, tags, and descriptions — perfect for engineers, students, tech enthusiasts, or anyone curious about what's inside a smartwatch.

---

##  Features

| Feature | Description |
|---------|-------------|
|  **Live Search** | Filter components by name, description, or any spec keyword (e.g., "ECG", "AMOLED", "LPDDR4X") |
|  **Category Filters** | One‑click buttons to show only Core, Display, Sensors, Power, or Connectivity modules |
|  **Responsive Design** | Works seamlessly on desktops, tablets, and mobile phones |
|  **Modern UI** | Glassmorphic header, smooth hover animations, intuitive card layout |
|  **Detailed Specs** | Each card includes a structured specs list + compact tech tags |
|  **No Dependencies** | Pure HTML/CSS/JS — no frameworks, no build step |
|  **Accessible** | Semantic HTML, ARIA‑friendly icons, keyboard navigable filters |

---

## 🗂️ Component Database

The website currently includes these **12 hand‑curated components**:

| ID | Component | Category | Key Specs |
|----|-----------|----------|-----------|
| 1 | System‑on‑Chip (SoC) | Core | Apple S9 / Snapdragon W5+, 4nm, dual‑core |
| 2 | RAM & Storage | Core | 1‑2GB LPDDR4X, 32‑64GB eMMC |
| 3 | AMOLED Display | Display | 1.43", 466x466, 1000+ nits |
| 4 | Haptic Engine & Crown | Display | LRA actuator, optical encoder |
| 5 | Optical HR & SpO₂ | Sensors | 8‑LED PPG, ±2 bpm accuracy |
| 6 | ECG Sensor | Sensors | Single‑lead, FDA/CE certified |
| 7 | IMU + Barometer | Sensors | 6‑axis accel/gyro, altimeter |
| 8 | Skin Temp & ALS | Sensors | ±0.1°C, under‑display ambient light |
| 9 | Li‑Po Battery | Power | 300‑600 mAh, 3.85V, 800 cycles |
| 10 | Wireless Charging | Power | Qi / magnetic, 2‑5W |
| 11 | Multi‑band GPS | Connectivity | L1+L5, Galileo, cold start <30s |
| 12 | Bluetooth + Wi‑Fi + NFC | Connectivity | BT 5.3, 2.4/5GHz Wi‑Fi, payments |

*Want more components? Open an issue or submit a PR — contributions welcome!*

---

## 🖼️ Screenshots

> *(Replace these placeholders with actual screenshots of your website)*

| Desktop View | Mobile View |
|--------------|--------------|
| ![Desktop Screenshot](https://via.placeholder.com/800x450?text=Desktop+View+of+Component+Grid) | ![Mobile Screenshot](https://via.placeholder.com/300x500?text=Mobile+View) |
| *Filter chips + search bar* | *Responsive cards stack vertically* |

---

## 🚀 Getting Started

You can run this project locally in **two clicks** — no server required.

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- (Optional) A text editor if you want to customize

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/smartwatch-component-atlas.git
   ```

2. **Navigate to the project folder**
   ```bash
   cd smartwatch-component-atlas
   ```

3. **Open the website**
   - Double‑click `index.html` — it will open in your default browser.
   - Or use a live server (VS Code extension: "Live Server").

No build tools, no `npm install` — just pure web standards.

---

## 💡 Usage

### Searching
- Type any keyword into the **search bar** (e.g., "gyroscope", "LPDDR", "waterproof").
- The grid updates instantly — matches are found in component name, description, specs list, and detail fields.

### Filtering
- Click any **category chip** (Core, Display, Sensors, Power, Connectivity).
- Active filter is highlighted in blue.
- Click **"All"** to reset.

### Reading a Component Card
- **Header:** Icon + category badge
- **Title:** Component name
- **Description:** What it does
- **Specs List:** Key technical values (clock speed, battery capacity, etc.)
- **Tech Tags:** Quick‑scan attributes (e.g., "L1+L5 GPS", "Always‑on mode")

---

## 🛠️ Customization

### Adding a New Component
Open `index.html` and locate the `componentsData` array (inside the `<script>` tag). Add a new object:

```javascript
{
    id: 13,
    name: "Your Component Name",
    category: "sensors",  // one of: core, display, sensors, power, connectivity
    icon: "fa-microchip", // Font Awesome 6 class
    description: "Brief explanation of the component...",
    specs: ["Spec 1", "Spec 2", "Spec 3"],
    details: {
        "Parameter 1": "Value 1",
        "Parameter 2": "Value 2"
    }
}
```

### Changing Colors / Theme
Modify the CSS variables at the top of the `<style>` block:

```css
.hero {
    background: linear-gradient(135deg, #0b1a2e 0%, #0f212f 100%);
}
.filter-chip.active {
    background: #1e6dc7;
}
```

### Exporting Data
The component database is plain JavaScript — you can easily copy it to a JSON file or integrate with a backend.

---

## 🧰 Technologies Used

- **HTML5** – Semantic structure, responsive meta tags
- **CSS3** – Flexbox, Grid, custom properties, modern transitions
- **JavaScript (ES6)** – Filtering, search, dynamic rendering, event handling
- **Font Awesome 6** – Icons for each component and UI element
- **Google Fonts (Inter)** – Clean, readable typography

No frameworks, no external libraries except icons and fonts.

---

## 🗺️ Roadmap

- [ ] Add dark/light theme toggle  
- [ ] "Compare Components" table (select 2‑3 cards side‑by‑side)  
- [ ] Download spec sheet as PDF  
- [ ] Add 3D smartwatch model with tooltips (Three.js)  
- [ ] Expand database: microphone, speaker, eSIM module, waterproofing gaskets  
- [ ] Interactive quiz: "Guess the component"  

*Have a suggestion? Open an issue or start a discussion!*

---

## 🤝 Contributing

Contributions are what make the open source community amazing. Any contributions you make are **greatly appreciated**.

1. **Fork the Project**
2. **Create your Feature Branch**  
   `git checkout -b feature/AmazingFeature`
3. **Commit your Changes**  
   `git commit -m 'Add some AmazingFeature'`
4. **Push to the Branch**  
   `git push origin feature/AmazingFeature`
5. **Open a Pull Request**

Please ensure your code follows the existing style (clean HTML/CSS/JS, no external dependencies).

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` file for more information.

You are free to use, modify, and distribute this project for personal or commercial purposes, as long as attribution is given.

---

## 🙏 Acknowledgments

- **Font Awesome** for the beautiful icon set  
- **Google Fonts** for the Inter typeface  
- All hardware engineers who document wearable tech publicly  
- The open source community for endless inspiration

---

## 📬 Contact

**Your Name** – [@yourtwitter](https://twitter.com/yourtwitter) – email@example.com  

Project Link: [https://github.com/yourusername/smartwatch-component-atlas](https://github.com/yourusername/smartwatch-component-atlas)
