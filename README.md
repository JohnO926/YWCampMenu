# YW Camp Meal Planner

Camp cooking coordination for Stake YW Camp, June 29 – July 2, 200 people.
Coordinated by John & wife, Logan Utah area.

## Quick Start

Open `yw_camp_planner.html` in any browser — no build step, no server, no dependencies.

## Files

```
yw-camp/
├── CLAUDE.md                  ← Full project context (Claude Code reads this automatically)
├── README.md                  ← This file
├── yw_camp_planner.html       ← Interactive meeting tool (open directly in browser)
├── YW_Camp_Meal_Plan.xlsx     ← Spreadsheet: Menu Plan, Shopping List, Prep Schedule
├── data/
│   └── meals.js               ← Meal library as a JS module (source of truth for meal data)
└── build_spreadsheet.py       ← Regenerates the .xlsx from scratch
```

## What the web app does

- **Meal Plan tab**: 4-day grid, click any meal to swap it
- **Shopping List tab**: auto-aggregates all ingredients across scheduled meals
- **Prep Schedule tab**: day-by-day task list, updates when meals change
- **Budget tab**: live cost estimate (Sam's Club + Costco pricing)

## Regenerating the spreadsheet

```bash
pip install openpyxl
python build_spreadsheet.py
```

## Adding a new meal option

Edit `data/meals.js` — add a new key to `MEAL_LIBRARY` following the existing structure,
then copy the updated data into the `ML` object inside `yw_camp_planner.html`.

## Current menu at a glance

| Day | Meal | |
|-----|------|-|
| Mon Jun 29 | Dinner | Taco Bar |
| Tue Jun 30 | Breakfast | Pancake Station |
| Tue Jun 30 | Lunch | Sub & Sandwich Bar |
| Tue Jun 30 | Dinner | **Hawaiian Haystacks** |
| Wed Jul 1 | Breakfast | Breakfast Burrito Bar |
| Wed Jul 1 | Lunch | **Teriyaki Protein Bowl** (Salad Spot inspired) |
| Wed Jul 1 | Dinner | **Pulled Pork + Dutch Oven Potatoes** |
| Thu Jul 2 | Breakfast | Muffins & Yogurt (grab & go) |

Estimated total: ~$3,900 · ~$19.50/person · ~$2.45/meal/person
Shopping: Sam's Club (most proteins) + Costco (pork shoulder ~$2.49/lb)
