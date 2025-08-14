```bash
██      ██ ██████  ██████  ███████ ███████ ████████  █████  ████████ ███████ 
██      ██ ██   ██ ██   ██ ██      ██         ██    ██   ██    ██    ██      
██      ██ ██████  ██████  █████   ███████    ██    ███████    ██    ███████ 
██      ██ ██   ██ ██   ██ ██           ██    ██    ██   ██    ██         ██ 
███████ ██ ██████  ██   ██ ███████ ███████    ██    ██   ██    ██    ███████ 
                your data, your freedom — Contribute today!
```

# Contributing to LibreStats

First off — **thank you** for considering contributing to **LibreStats**!  
This is a community driven, open source project with one mission: **your data, your freedom...**  
We believe in making high quality datasets freely available for everyone — researchers, engineers, students and data enthusiasts worldwide.  

This guide will help you understand how to contribute datasets, improve existing ones or help with code.

---

## Steps to Contribute

Let’s walk through it with a live example using **LibreStats/LibreStats** repository.

### 1. Fork the Repository
Go to: [https://github.com/LibreStats/LibreStats](https://github.com/LibreStats/LibreStats)  
Click **Fork** to create your own copy under your GitHub account.  
Example fork: `your-github/LibreStats`

### 2. Clone the Fork Locally
```bash
git clone https://github.com/your-github/LibreStats.git
cd LibreStats
```

### 3. Create a New Branch
Never work directly on the `main` branch.
```bash
git checkout -b my-new-dataset
```

### 4. Keep Your Main Branch Updated
Before making changes, ensure your local `main` is up to date with the original repo:
```bash
git remote add upstream https://github.com/LibreStats/LibreStats.git
git checkout main
git pull upstream main
```

### 5. Make Your Changes
Add your dataset (following the [Rules of Contribution](#rules-of-contribution) below) or update existing files.

### 6. Stage & Commit
```bash
git add .
git commit -m "Added GDP by country dataset under economics domain"
```

### 7. Push Your Branch
```bash
git push origin my-new-dataset
```

### 8. Open a Pull Request
Go to your fork on GitHub → click Compare & pull request → submit.

### 9. Resolve Merge Conflicts (if any)
```bash
git fetch upstream
git merge upstream/main
# Fix conflicts in files
git add .
git commit
git push origin my-new-dataset
```
Then update your pull request.

---

## Rules of Contribution

### 1. Folder Structure
* All datasets go inside the `datasets/` folder under a domain name
* If the domain exists, put your dataset there
* If not, create a new domain folder

Examples:
```bash
datasets/economics
datasets/privacy
datasets/climate_change
```
Domain naming rules:
- Single words in lowercase (e.g., economics, privacy).
- If two or more words, use snake_case (e.g., climate_change).

### 2. Dataset Naming
* CSV format only (.csv)
* Snake_case naming
* Always end with `_data.csv`

Example:
```bash
datasets/awards/fields_medal_winners_data.csv
```

### 3. Metadata File
Every dataset must have a `.meta.json` file with the exact same name as the CSV but with `.meta.json` extension.

Example:
```bash
fields_medal_winners_data.meta.json
```
**Why?**
This metadata gives important details like dataset title, description, sources, contributors, and last update date.

**Metadata format example:**
```bash
{
  "title": "Fields Medal Winners by Country and Year",
  "description": "Aggregated data of Fields Medal awards, showing the number of recipients from each country for each year.",
  "source": [
    "https://www.mathunion.org/imu-awards/fields-medal"
  ],
  "contributors": [
    {
      "name": "Alex",
      "email": "malexben443@gmail.com"
    }
  ],
  "last_updated": "12-08-2025"
}
```
* Multiple sources? Add each URL in `"source"` separated by commas.
* Adding to an existing dataset? Add your name/email to `"contributors"` (don’t remove others).
* Always update `"last_updated"` to the date you make changes (`DD-MM-YYYY` format).
* You can fix incorrect data — but you must provide verified sources for changes.

---

🌍 Why Contribute?
By contributing, you help build a free, open and powerful repository of datasets — a resource that can fuel research, innovation and learning across the globe.

---

❤️ Let’s Build This Together!<br>Fork it.<br>Clone it.<br>Make data open.

GitHub: https://github.com/LibreStats<br>Follow this project on LinkedIn: https://www.linkedin.com/company/librestats

**your data, your freedom...**


