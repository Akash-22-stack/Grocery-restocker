
# 🧠 Smart Grocery Shelf Restocker (Object Detection ML Project)

## 📌 Overview

This project solves a real-world problem faced by homes, hostels, and small shops: **forgetting to restock essential grocery items**. Using computer vision and object detection, this tool analyzes an image of a grocery shelf or kitchen cabinet and identifies:

- ✅ Items currently present
- ⚠️ Items that are low in quantity
- ❌ Items that are completely missing

It then generates an intelligent **restocking list** to help users buy only what’s needed.

---

## 🎯 Problem Statement

In everyday life, people often run out of essential groceries because they can't track what's left in their storage. By simply clicking a photo of their shelf:

- The model detects known grocery items
- Flags those that are low in stock (visually less than 50% full or small in size)
- Flags missing items (not detected in the image at all)
- Outputs a clear and structured restock recommendation

---

## 🧾 Target Grocery Items

We focus on 6 common grocery items:

- 🥛 Milk Carton
- 🍞 Bread Loaf
- 🥚 Egg Tray
- 🥣 Cereal Box
- ☕ Coffee Bottle
- 💧 Water Bottle

The system identifies them in the image and applies simple logic:
- Items **not detected** = **Missing**
- Items **detected but small or half-full** = **Low Stock**

---

## 🔄 Output Format

After analyzing the image, the system generates an output like:

```json
{
  "Detected_Items": ["Milk", "Bread", "Water Bottle"],
  "Low_Stock_Items": ["Milk", "Water Bottle"],
  "Missing_Items": ["Eggs", "Cereal", "Coffee"],
  "Restock_Recommendation": ["Eggs", "Cereal", "Coffee", "Milk", "Water Bottle"]
}
