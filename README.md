# MyAnimeList Character Voting Analysis

This project analyzes audience preferences for anime and manga characters based on voting data from [MyAnimeList](https://myanimelist.net/character.php). The goal is to uncover patterns in popularity and infer demographic details, such as gender, from available information.

🔗 **Final Results**: [View the interactive visualizations](https://yiren54610.github.io/project_5/)

---

## 📊 Methodology

This is a scraping-intensive project that focuses on characters who received more than **1,000 votes**.

### Data Collection

- **Beautiful Soup** was used to extract:
  - Character name
  - Profile link
  - Number of votes
  - Associated anime or manga

- **Playwright** was used to navigate to each character's individual page and capture:
  - Biographical description
  - Image source link

- The scraped data was saved into a structured `.csv` file for further analysis.

---

## 🧠 Description & Gender Analysis

Because gender is not directly listed on character pages, a custom script was used to infer gender from textual descriptions.

### Extraction Process

- Used **regular expressions** to extract:
  - Age
  - Birthday
  - Nationality
  - Height
  - Occupation
  - Biography paragraph

### Gender Inference

A scoring system was developed based on the presence of gendered keywords:

- **Female indicators**: `['she', 'her', 'woman', 'girl', 'female', 'lady']`  
- **Male indicators**: `['he', 'him', 'man', 'boy', 'male', 'gentleman']`

- Each detected keyword adds one point to the corresponding gender score.
- Gender is inferred based on the higher total score.
- The result is stored in a new column titled `gender` in the CSV.

---

## 📈 Data Visualization

Two main types of visualizations were created to explore trends:

### Beeswarm Chart

- Created using **RawGraphs**
- Exported as an **SVG**
- Designed responsively using **Adobe Illustrator** + **ai2html**

### Scatter Plot

- Built with **Datawrapper**
- Characters are color-coded based on inferred gender

---

## 🛠 Tools & Libraries

- Python  
  - `BeautifulSoup`  
  - `Playwright`  
  - `re` (regular expressions)  
  - `pandas`  
- Visualization  
  - RawGraphs  
  - Datawrapper  
  - Adobe Illustrator  
  - ai2html

---



 
