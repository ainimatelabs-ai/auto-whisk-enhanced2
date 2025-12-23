# 🎯 Auto Whisk Enhanced v8.5.0

**Smart AI Image Generation Tool with Advanced Reference Filtering**

![Python](https://img.shields.io/badge/Python-3.11-blue)
![PySide6](https://img.shields.io/badge/PySide6-6.6.1-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## ✨ Features

### 🎯 Smart Filtering System
- **Automatic reference selection** based on prompt keywords
- **Name-based matching** - Characters mentioned by name are always included
- **Tag-based filtering** - References matched by comma-separated tags
- **Caption analysis** - AI-generated captions used for semantic matching

### ➕ Dynamic Reference Slots
- **Unlimited subjects** - Add as many characters as needed
- **Unlimited scenes** - Add multiple location references
- **Easy management** - Add/remove slots with + and × buttons

### 🏷️ Rich Metadata System
- **Name field** - Identify references by name
- **Tags field** - Comma-separated keywords for smart matching
- **Caption field** - AI-generated descriptions (editable)

### 🌍 Multi-language Support
- 🇹🇷 Turkish (Türkçe)
- 🇺🇸 English
- 🇻🇳 Vietnamese (Tiếng Việt)

### 🎨 Modern Qt6 Interface
- Clean, professional UI design
- Responsive layout with drag-and-drop support
- Real-time progress tracking
- Batch processing with queue management

---

## 📥 Download

### Windows EXE (Ready to Use)

**Latest Release:** [Download AutoWhisk_Enhanced_v8.5.exe](../../releases/latest)

No Python installation required! Just download and run.

---

## 🚀 Quick Start

### For EXE Users:

1. **Download** the EXE from releases
2. **Get your cookie:**
   - Visit https://labs.google/fx/tools/whisk
   - Login to your Google account
   - Use [Cookie Exporter](https://chrome.google.com/webstore/detail/cookie-exporter/) extension
   - Export as JSON
3. **Run the program:**
   - Paste cookie JSON
   - Click "Check & Save"
   - Start creating!

### For Python Users:

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/auto-whisk-enhanced.git
cd auto-whisk-enhanced

# Install dependencies
pip install PySide6 requests pyinstaller

# Run
python auto_whisk_enhanced_v8.5.py
```

---

## 📖 How Smart Filtering Works

### Priority System:

1. **Name Matching (Highest Priority)**
   - Prompt: "Ahmet and Ali playing football"
   - → Selects ALL references named "Ahmet" and "Ali"
   - No limit on name matches!

2. **Tag Matching (High Priority)**
   - Reference tags: `hero, warrior, strong`
   - Prompt: "A brave warrior fighting"
   - → Selected (tag: warrior)

3. **Caption Matching (Medium Priority)**
   - Caption: "A young man wearing blue shirt"
   - Prompt: "Someone in a blue shirt"
   - → Selected (keywords: blue, shirt)

4. **Scene Matching (OR Logic)**
   - Any scene with matching keywords is included

5. **Style Matching (OR Logic)**
   - Any style reference with matches is included

---

## 📋 Example Usage

### Setup References:

**Subject 1:**
- Name: `Ahmet`
- Tags: `man, hero, brown-hair`
- Caption: `A brave young man with brown hair`

**Subject 2:**
- Name: `Ayşe`
- Tags: `woman, doctor, glasses`
- Caption: `A professional woman wearing glasses`

**Scene:**
- Name: `Park`
- Tags: `outdoor, nature, trees`
- Caption: `A beautiful park with green trees`

### Generate Images:

**Prompt 1:** `"Ahmet and Ayşe walking in the park"`
- ✅ Selected: Ahmet (name match)
- ✅ Selected: Ayşe (name match)
- ✅ Selected: Park (tag: park)

**Prompt 2:** `"A doctor examining a patient"`
- ✅ Selected: Ayşe (tag: doctor)
- ❌ Ahmet (no match)
- ❌ Park (no match)

**Prompt 3:** `"A hero fighting in the forest"`
- ✅ Selected: Ahmet (tag: hero)
- ❌ Ayşe (no match)
- ❌ Park (no forest tag)

---

## 🛠️ Build from Source

### Requirements:
- Python 3.9+
- PySide6 6.6.1
- requests 2.31.0
- pyinstaller 6.3.0

### Build EXE:

```bash
# Install dependencies
pip install PySide6 requests pyinstaller

# Build
pyinstaller --onefile --windowed --name="AutoWhisk_Enhanced_v8.5" auto_whisk_enhanced_v8.5.py

# Find EXE in dist/ folder
```

---

## 📝 License

MIT License - Feel free to use and modify!

---

## 🙏 Credits

**Original Auto Whisk:** [Duck Martians](https://github.com/duckmartians)

**Enhanced Version:** Smart filtering and dynamic slots added

---

## ☕ Support

If you find this useful:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow)](https://buymeacoffee.com/duckmartians)

---

## 🐛 Issues & Feedback

Found a bug? Have a suggestion?

[Open an Issue](../../issues/new)

---

**Star ⭐ this repo if you like it!**
