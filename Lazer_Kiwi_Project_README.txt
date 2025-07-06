# Lazer Kiwi Dota 2 Guild Website – Project README

Welcome to the modular, multi-tab website for the Lazer Kiwi Dota 2 guild. This site is built for presenting guild statistics, rankings, and player comparisons through clean visuals, interactive tools, and live Google Sheets integrations.

---

## 🔧 Modules Overview

| Module                             | Purpose                                                        | Filename                                      |
|------------------------------------|----------------------------------------------------------------|-----------------------------------------------|
| Home Page                          | Welcome text, news feed, AI Kiwi art gallery                   | `Home_Page_MASTER.html`                       |
| Turbo Rank Graphs                  | Line graphs of turbo rank progression over time                | `Turbo_Rank_Graphs_MASTER.html`              |
| Party Average Rank Estimator       | Dropdown selector to estimate 5-player party rank              | `Party_Average_Rank_Estimator_MASTER.html`    |
| Weekly Guild Point Leaderboard     | Weekly point gains, sortable table, 4-week average toggle      | `Weekly_Guild_Point_Leaderboard_MASTER.html`  |
| Weekly Point Earning Graphs        | Graph comparing weekly points for 2 selected members           | `Weekly_Point_Earning_Graphs_MASTER.html`     |
| Guild Estimated Turbo Rank List    | Rank estimates for all visible members from recent Turbo data  | `Guild_Estimated_Turbo_Rank_List_MASTER.html` |
| Main Index Page                    | Integrates all tabs and banner into a cohesive UI              | `index.html`                                  |

---

## 🌐 Live Data Endpoints

These Google Apps Script endpoints feed live JSON data to different modules:

| Use Case                        | URL                                                                                             |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| Turbo Rank Snapshots            | `https://script.google.com/macros/s/AKfycbzAOfvSd1CvLTCRj6YLlDLQEJSkfXHxvKE0PIhl5iU9gtTg3fVoE3mCn2M_aCI1OzL0hw/exec` |
| Weekly Points (Leaderboard + Graphs) | `https://script.google.com/macros/s/AKfycbz3txnsBI5fLUtGxuw2RwvUTlfTthoyNiufE3pdxEa0F4ESsMoN439s85T2C2da1Mg/exec` |
| Total Points + 3-Week Avg       | `https://script.google.com/macros/s/AKfycbxCm2fdYwdu-EHsDAT2AxnO6NsZ2d_mkg-4Meke-FTRBxTGEF5AmwLPifcbFOn5lYQY/exec` |
| Visit Counter (Home Page)       | `https://script.google.com/macros/s/AKfycbztKjPJahRvifOZBqlOA890PBXK5AqAqv2VksE7A1JlAHN84gQ98mxVjwDi98K6Sn6nsg/exec` |
| News & Updates Feed             | `https://script.google.com/macros/s/AKfycbzO8o3mKTDxHg5L2FGYe_ClEQtVZDy2HTW1JkXGsF5XJEbFNIoKejOU4jSDJGzMfqyXMg/exec` |

---

## 🎨 Styling & Design

- **Font**: Orbitron (via Google Fonts)
- **Colors**:
  - Background: `#000000`
  - Text/Highlight: `#00FF00` (neon green)
  - Accent/Borders: `#ab6e11` (burnt orange)
- **Kiwi Branding**: Includes `kiwi.png` and AI-generated images
- **Graph Lines**:
  - Player 1: Cyan `#00FFFF`
  - Player 2: Pink `#FF6699`
- **Style Themes**:
  - Tabs and buttons with neon glows
  - Futuristic font and layouts
  - Hover and blink effects for interactivity

---

## 🧱 Site Structure and Behavior

- `index.html` integrates all modules using `<iframe>`s under a tabbed navigation bar.
- The banner image (`Banner.png`) is located at `home_gallery_assets/Banner.png`.
- Tab content is styled and loaded efficiently without page reloads.
- All scripts are inline within HTML for simplicity and performance.
- Each module is responsible for one self-contained task, using live data where possible.

---

## 🔄 Special Behaviors

- **Leaderboard Columns**:
  - Toggle reveals/hides Total and Avg columns.
  - Columns adapt based on the week selected.
- **News Feed**:
  - Sorted by date (newest at top).
  - Multiple posts on the same day are reversed so latest appears first.
- **Rank Calculators**:
  - Turbo averages are taken from most recent 15 solo matches (where public data is available).
- **Charts**:
  - Line graphs adapt to selected players and dates.
  - Custom min/max Y-axis bounds per player.

---

## 📁 File Conventions

- Master files use the `_MASTER.html` suffix.
- Any edits must go through versioning (e.g., `_v2.html`, `_PATCHED_FIXED.html`).
- Final working files confirmed by the user are marked with `_FINAL_FIXED.html`.


---

## 🚧 Future Ideas

- Add Dota 2 stats overlays (e.g., win rate)
- Discord bot integration for live leaderboard pings
- Guild member bios / profile pages
- Automated match scraping updates

---

Maintained by the Bag of Dicks. Updates and ideas welcome via Discord.
