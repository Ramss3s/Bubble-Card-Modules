# 🫧 Bubble Card Modules

A curated collection of advanced, custom modules designed for [Bubble Card](https://github.com/Clooos/Bubble-Card) in Home Assistant, created and maintained by **[Ramss3s](https://github.com/Ramss3s)**.

---

## 📦 Available Modules

### 1. 🛋️ Bubble Area Card v3
**File:** [`bubble_area_card_v3.yaml`](./bubble_area_card_v3.yaml)  
**Target Card:** `button` (transforms a standard button card into an all-in-one smart room controller)  
**Version:** `v3.0.0`

#### ✨ Highlights:
* 📐 **4 Versatile Layouts:**
  * **Compact Vertical:** Native Home Assistant dashboard proportions.
  * **Horizontal Capsule:** Single-row 54px pill layout inspired by native Bubble buttons.
  * **Square (1:1):** Symmetric grid tile for tablets and multi-column views.
  * **Minimalist:** Ultra-clean icon & room title only.
* 🚨 **Dynamic Alert Icon Replacement:**
  * The main room icon dynamically switches to the active hazard/alert (`mdi:fire`, `mdi:water`, `mdi:motion-sensor`, `mdi:door-open`, `mdi:window-open-variant`, `mdi:air-filter`, `mdi:battery-alert`).
  * Real-time luminous backlight halos (Crimson red, Cyan, Amber, Purple) and expanding presence radar pulse waves.
* 🎛️ **Interactive Touch & Drag Slider:**
  * Micro progress bar along the bottom edge for immediate 60fps brightness & volume adjustment without opening popups.
  * Double-tap the bar or light chip to instantly swap between controlling room lights and media player volume.
* 💡 **Ambient Lighting Glow & Glowing Capsule:**
  * Organic breathing aura that auto-syncs with RGB light colors and color temperatures.
  * Frosted glass top-right capsule with glowing amber micro-dots showing the exact count of active lights.
* 🎵 **Four-Corner Acoustic Waves:**
  * Smooth organic waves expanding from all 4 corners when music is playing.
* 🌡️ **Thermostat Status Chip:**
  * Frameless top-left status chip showing heating/cooling icon and target temperature (e.g. `🔥 22°`).
* 📜 **Apple-Style Marquee:**
  * Smooth ping-pong auto-scrolling when subtitle sensors text overflows the card width.
* ⚙️ **100% GUI Configurable:**
  * Includes a built-in **Test State Preview** gallery dropdown to test alerts, music waves, and dual sliders without triggering physical sensors.

---

## 🚀 Installation

1. Make sure you have [Bubble Card](https://github.com/Clooos/Bubble-Card) (v2.3.0+) installed via HACS.
2. Download [`bubble_area_card_v3.yaml`](https://raw.githubusercontent.com/Ramss3s/Bubble-Card-Modules/main/bubble_area_card_v3.yaml).
3. Place the YAML file into your Home Assistant configuration directory, for example:
   * `/config/www/bubble/bubble-modules.yaml` (or your preferred modular YAML directory).
4. In your Home Assistant dashboard, add a standard **Bubble Button Card** and select **Bubble Area Card v3 (Ramss3s)** from the module dropdown in the visual editor.

---

## ⚙️ Example Configuration

```yaml
type: custom:bubble-card
card_type: button
button_type: state
entity: light.living_room
modules:
  - ramss3s_area_v3
ramss3s_area_v3:
  area: living_room
  card_layout: horizontal # options: vertical, square, horizontal, minimal
  enable_light_glow: true
  glow_style: center_aura
  show_edge_bar: true
  edge_bar_mode: auto
  show_media_waves: true
  show_temperature: true
  show_humidity: true
  show_alerts: true
```

---

## 🤝 Community & Support

* Discuss and share feedback on the [Bubble Card Community Discussions](https://github.com/Clooos/Bubble-Card/discussions/categories/share-your-modules).
* Created with ❤️ by **[Ramss3s](https://github.com/Ramss3s)**.
