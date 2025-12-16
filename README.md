#🚀 LeadForge - Conversion Simulator**LeadForge** is a single-page interactive application designed to visualize the "Cost of Inaction" in sales and marketing. It simulates how response time ("Speed to Lead") and operational friction impact revenue capture.

This tool is built to demonstrate the exponential decay of lead value over time, helping businesses understand the ROI of implementing automation and CRM systems.

---

##✨ Features* **Real-Time Simulation:** Instantly calculates "Captured Revenue" vs. "Money Left on Table" as you adjust lead volume and deal value.
* **Decay Curve Visualization:** Uses **Plotly.js** to render a dynamic graph showing how lead conversion probability drops minute-by-minute.
* **Gamified System Stack:** Users can add or remove "Friction Points" (e.g., *No CRM*, *Manual Data Entry*) or "Efficiency Boosters" (e.g., *Calendar Booking*) to see how their tech stack affects their bottom line.
* **AI Speed-to-Lead Mode:** A dedicated toggle to simulate instant response times, showing the maximum theoretical revenue ceiling.
* **Responsive UI:** A modern, mobile-friendly interface styled with a professional "MarTech" aesthetic.

##🛠️ Tech Stack* **Core:** HTML5, CSS3, Vanilla JavaScript (ES6+).
* **Visualization:** [Plotly.js](https://plotly.com/javascript/) (via CDN).
* **Icons:** [FontAwesome](https://fontawesome.com/) (via CDN).
* **No Build Step:** Zero dependencies or build processes required. Runs directly in the browser.

##🚀 Quick Start1. **Download** the `index.html` file.
2. **Open** the file in any modern web browser (Chrome, Firefox, Safari, Edge).
3. **Ensure** you have an active internet connection (required to load Plotly and FontAwesome from CDNs).

##🧮 How It Works (The Math)The simulator uses an **Exponential Decay Model** to calculate revenue based on time.

###The FormulaThe conversion rate (C) at time (t) is calculated as:

* **t (Time):** Minutes passed since the lead came in.
* **k (Decay Speed):** This is determined by the "Friction Score."
* *High Friction* (e.g., Manual entry, No CRM) = Higher k (Steep drop-off).
* *Low Friction* (e.g., AI Tools, Scoring) = Lower k (Flatter curve).



###The Logic1. **Base Conversion:** Assumes a standard 5% conversion rate for instant contact.
2. **Friction Modifiers:** Selecting items in the "System" tab modifies the friction score.
3. **Response Time:**
* **Manual Mode:** Assumes a 30-minute delay + friction penalties.
* **AI Mode:** Assumes a <1 minute response time.



##⚙️ ConfigurationYou can easily customize the "Friction Points" (the items in the System tab) by editing the `config` object inside the `<script>` tag:

```javascript
const config = {
    presets: [
        // value: Negative numbers hurt conversion, Positive numbers help it.
        { id: 1, name: 'Manual Data Entry', value: -15, icon: '⌨️', desc: 'Slow response' },
        { id: 2, name: 'Lead Scoring', value: 10, icon: '🎯', desc: 'Focus on best' },
        // Add your own items here...
    ]
};

```

##🎨 CustomizationThe design relies on CSS Variables for easy theming. Look for the `:root` section in the `<style>` block:

```css
:root {
    --primary: #8b5cf6;       /* Main Theme Color */
    --secondary: #10b981;     /* Success/Green */
    --loss-color: #ef4444;    /* Loss/Red */
    --radius: 16px;           /* UI Roundness */
}

```

##🤝 Contributing1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/NewFeature`).
3. Commit your changes.
4. Push to the branch.
5. Open a Pull Request.

##📄 LicenseDistributed under the MIT License. See `LICENSE` for more information.
