# 🏰 Urthan: The Infinite Kingdoms

**Made by Satoru Suzuki**

A high-performance, single-file procedural world engine designed for high-fantasy exploration and grand strategy. This engine simulates an infinite realm where every tile represents a **1x1 km area**, governed by complex geological and climatic noise layers.

Building on the same flexible architecture as *Frostward*, this tool provides a foundation for infinite fantasy maps, kingdoms, and chronicles without the need for external assets or heavy engines.

---

## 📜 The Urthan Logic

The world of Urthan is generated through **Triple-Layer Noise Abstraction**, creating realistic ecological transitions across infinite coordinates:

1.  **Elevation ($e$):** Defines the physical structure of the world, from **Abyssal Oceans** to the oxygen-thin **Gods Peaks**.
2.  **Moisture ($m$):** Dictates the humidity of the land, separating the **Great Deserts** from the **Festering Swamps** and **Rainforests**.
3.  **Temperature ($t$):** Creates latitudinal climate zones, ranging from tropical **Savannas** to the frozen **Boreal Forests** and **Tundras**.

---

## ✨ Key Features 

* **🌐 Infinite Procedural Exploration:** Uses **Fractal Brownian Motion (FBM)** with 4 octaves to generate natural coastlines, mountain ranges, and biomes.
* **🏛️ Sector-Based Capital Logic:** Features a sophisticated spawning system that ensures a **High Capital** (or **Sunken Capital**) appears once every 30x30 km sector, providing strategic points of interest.
* **✒️ The Chronicles:** A built-in coordinate-based ledger (journal) that allows cartographers to record local history, resources, or political allegiances on specific tiles.
* **💾 Persistent Save System:** Integrated `localStorage` support. Your current location ($X, Y$), the **World Seed** (Year), and all journal entries are automatically saved.
* **📜 Centralized Chronicle Reviewer:** A dedicated interface to review all recorded notes from across the infinite world in one chronological list.
* **🔑 Custom Seed Injection:** Players can manually load specific world seeds, referred to as the **"Year of the Third Era,"** to explore shared world states.
* **⚙️ Unified Realm Menu:** A clean modal UI for managing saves, reviewing chronicles, and performing "Astral Travel".
* **💯 Zero-Dependency Architecture:** A single HTML file containing all Logic (JS), Styling (CSS), and Structure (HTML).

---

## 🎮 Controls

* **Navigation:** Use `WASD` or `Arrow Keys` to travel across the map.
* **📜 Survey (Journal):** Click your current tile to read geographical data and scribe an entry in the **Chronicles**.
* **⚙️ Realm System:** Access the settings icon to save progress, review logs, or jump to new coordinates.
* **✨ Astral Travel:** A magical teleportation protocol that allows you to jump thousands of kilometers to a new random kingdom.
* **🔥 New Age:** Permanently end the current era to generate a completely new world seed and history.

---

## 🗺 Kingdom & Biome Reference

| Icon | Name | Description | Logic Condition |
| :--- | :--- | :--- | :--- |
| 🏛️ | **High Capital** | The seat of kings and center of power. | Sector-based Unique Spawn |
| 🔱 | **Sunken Capital** | A kingdom claimed by the sea. | Sector Point + Low Elevation |
| 🏰 | **Stone Keep** | A lord's fortified dominion. | High Elevation + Random Spawn |
| ⚓ | **Port City** | Coastal hub for maritime commerce. | Coastal Sea Edge ($e \approx 0.32$) |
| 🛕 | **Ancient Ruins** | Remnants of lost civilizations. | Rare Spawn (Desert/Swamp bias) |
| 🏔️ | **Gods Peak** | Summits where the air is thin. | Max Elevation ($e > 0.92$) |
| 🛖 | **Tribal Village** | Locals who know the wild's secrets. | Jungle, Swamp, or Forest |
| ⛺ | **Nomad Camp** | Wanderers resting for the night. | Desert, Steppe, or Tundra |

---

## 🚀 Deployment

1.  Download or clone the repository.
2.  Open `urthan-map.html` in any modern web browser.
3.  No server, build-tools, or installation required. 

---

> "History is not found in the books of the old, but in the soil of the lands we claim."
