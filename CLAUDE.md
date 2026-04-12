# YW Camp Meal Planner — Project Context

This project was started in a Claude.ai chat and moved to Claude Code. All decisions,
preferences, and context from that conversation are captured here.

---

## The Event

- **Event**: Stake Young Women's Camp (LDS church camp for teenage girls)
- **Coordinators**: John and his wife
- **Dates**: Monday June 29 – Thursday July 2
- **Headcount**: 200 people
- **Kitchen**: Decent camp kitchen available
- **Primary cooking equipment**: Flat top grill + oven + slow cookers + rice cookers

### Meal schedule
- Day 1 (Mon Jun 29): Dinner only
- Day 2 (Tue Jun 30): Breakfast, Lunch, Dinner
- Day 3 (Wed Jul 1): Breakfast, Lunch, Dinner
- Day 4 (Thu Jul 2): Breakfast only (departure day — easy cleanup)

---

## Core Philosophy

1. **Build-your-own / toppings bar style** for every meal — picky eaters can skip what they don't want
2. **Flat top or cook-ahead as much as possible** — minimize day-of complexity
3. **Slow cookers are gold** — overnight proteins, sauces that hold warm
4. **Variety across the menu** — no repeated proteins or flavor profiles back-to-back

---

## Current Menu (Locked In)

| Day | Meal | Name |
|-----|------|------|
| Day 1 — Mon Jun 29 | Dinner | Build Your Own Taco Bar |
| Day 2 — Tue Jun 30 | Breakfast | Pancake Station |
| Day 2 — Tue Jun 30 | Lunch | Sub & Sandwich Bar |
| Day 2 — Tue Jun 30 | Dinner | Hawaiian Haystacks ⭐ |
| Day 3 — Wed Jul 1 | Breakfast | Breakfast Burrito Bar |
| Day 3 — Wed Jul 1 | Lunch | Teriyaki Protein Bowl |
| Day 3 — Wed Jul 1 | Dinner | Pulled Pork + Dutch Oven Potatoes |
| Day 4 — Thu Jul 2 | Breakfast | Muffins & Yogurt (grab & go) |

### Key notes on specific meals

**Hawaiian Haystacks (Day 2 Dinner)**
- This replaced the original Baked Potato Bar (rejected — too hard to bake 200 potatoes)
- Classic Utah/LDS YW camp dish — the group will love it
- Sauce: cream of chicken soup + chicken broth + shredded chicken in slow cookers
- Toppings: shredded cheddar, pineapple chunks, mandarin oranges, coconut flakes,
  chow mein noodles, diced tomatoes, black olives, sour cream, green onions, celery

**Teriyaki Protein Bowl (Day 3 Lunch)**
- Inspired by Salad Spot restaurant in Logan, UT (john@valiflo.com is local to Logan area)
- Based on their Teriyaki Protein Bowl menu item
- Base: mixed grains (rice + quinoa), butter leaf lettuce
- Protein: seasoned chicken on flat top
- Toppings: shredded carrots, cucumbers, bell pepper, edamame, cilantro, black sesame seeds
- Sauces: teriyaki dressing + garlic aioli (in squeeze bottles)

**Pulled Pork (Day 3 Dinner)**
- Pork shoulder goes into slow cookers the night before (Tue night after dinner)
- 14–16 hour cook — ready to shred Wed morning
- Dutch oven potatoes: sliced russets, onion, bacon, butter, cheddar at 375°F for ~90 min

**Muffins & Yogurt (Day 4 Breakfast)**
- Specifically requested as no-cook, grab-and-go for departure morning
- Buy muffins from Costco ahead of time
- Individual yogurt cups + fresh fruit + juice boxes

---

## Meals That Were Considered and Rejected

These are in the meal library in the web app as swap options:

| Meal | Why Rejected |
|------|-------------|
| Baked Potato Bar | Too hard to bake 200 potatoes — oven logistics |
| Walking Tacos (Frito bags) | Too similar to Day 1 Taco Bar |
| Pasta Bar | Too hard to cook that much pasta at scale |
| Nachos | Rejected during dinner swap discussion |
| Chili Bar | Rejected during dinner swap discussion |
| BBQ Chicken Sandwich Bar | Conflicts with pulled pork already on Day 3 |
| Stir Fry Bowl Bar | Too similar to Day 3 Teriyaki Bowls |
| Sloppy Joe Bar | Considered but passed on |
| Chipotle Rice Bowl | Early draft version, replaced by Teriyaki Bowl |
| Mac & Cheese Bar | Considered but not selected |
| Flatbread Pizza Bar | Considered but not selected |

---

## Shopping

- **Primary stores**: Sam's Club + Costco (both in Logan, UT area)
- **Strategy**: Proteins at Sam's Club (better prices); pork shoulder at Costco (~$2.49/lb)
- **Estimated total**: ~$3,900 for all 8 meals / 200 people
- **Per person**: ~$19.50 | **Per meal/person**: ~$2.45

### Key price references (current as of early 2026)
- Ground beef 80/20: $4.58/lb (Sam's Club)
- Chicken breast: $2.77/lb (Sam's Club)
- Pork shoulder: $2.49/lb (Costco)
- Bacon: $3.49/lb (Sam's Club)
- Eggs: ~$4.00/dozen (bulk)
- Shredded cheddar: ~$4.00/lb bulk

---

## Prep Schedule Highlights

### Pre-camp (Sat Jun 28)
- All shopping at Sam's + Costco
- Wash & prep produce, portion spice blends

### Day 1 (Mon Jun 29 — arrival)
- Set up kitchen on arrival
- Cook taco proteins in afternoon
- After dinner: START PORK IN SLOW COOKERS for Day 3 dinner (overnight)

### Day 2 (Tue Jun 30)
- Early: flat top for pancake breakfast
- Morning: set up sandwich bar (no cook)
- Afternoon: prep Hawaiian Haystacks sauce + rice
- After dinner: Cook rice & quinoa for Day 3 teriyaki bowls (refrigerate overnight)

### Day 3 (Wed Jul 1)
- Early: flat top for breakfast burrito bar
- Morning: reheat grains, cook chicken for teriyaki bowls, lunch service
- Afternoon: shred pork, prep dutch oven potatoes in oven, dinner service

### Day 4 (Thu Jul 2 — departure)
- Set out muffins, yogurt, fruit, juice — no cooking at all
- Kitchen cleanup and pack out

---

## Files in This Project

| File | Description |
|------|-------------|
| `CLAUDE.md` | This file — full project context |
| `yw_camp_planner.html` | Standalone web app — open in browser for meetings |
| `YW_Camp_Meal_Plan.xlsx` | Spreadsheet with 3 tabs: Menu Plan, Shopping List, Prep Schedule |
| `data/meals.js` | Extracted meal library data (JS module) |
| `data/schedule.js` | Current schedule and day config |

---

## Web App Details (`yw_camp_planner.html`)

A fully self-contained single HTML file. No build step, no dependencies, no internet required.

**Features:**
- **Meal Plan tab**: 4-day grid, click any meal card to open swap panel
- **Shopping List tab**: auto-aggregates items across all meals, merged by item+unit
- **Prep Schedule tab**: organized by day, night-before tasks shift to prior day automatically
- **Budget tab**: live total in tab label, category bars, per-meal breakdown

**Swap panel**: Shows ALL meals of the same type (breakfast/lunch/dinner) including
rejected alternatives. Current meal is highlighted. Click any option to swap — all
4 tabs update immediately.

**To extend the app:**
- Add new meals to the `ML` object at the top of the `<script>` tag
- Each meal needs: `name, type, tags, desc, cook, shopping[], prep[]`
- `shopping` items need: `{item, qty, unit, uc (unit cost), cat}`
- `prep` items need: `{when, time, task, tip}` where `when` is one of:
  `'morning-of' | 'afternoon' | 'day-of' | 'night-before' | 'evening'`

---

## Spreadsheet Details (`YW_Camp_Meal_Plan.xlsx`)

Built with openpyxl. Three tabs:
1. **Menu Plan** — color-coded meal overview (breakfast=amber, lunch=blue, dinner=purple)
2. **Shopping List** — organized by category with quantities for 200 people
3. **Prep Schedule** — day-by-day from pre-camp through departure

To regenerate the spreadsheet after changes, run `build_spreadsheet.py`.

---

## John's Preferences & Context

- Located in Logan, Utah
- Shopping at Sam's Club + Costco
- Company: Valiflo (john@valiflo.com)
- Comfortable with flat top cooking, slow cookers, large-batch kitchen work
- Wants build-your-own style for every meal (picky eaters)
- Prefers cook-ahead or flat top over complex oven logistics
- Familiar with Claude Code and claude.ai web interface
