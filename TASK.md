# Family Tree Website Task

Build a beautiful, interactive family tree website using DaisyUI + Tailwind CSS.

## Data
- `persons.json` - 172 family members with relationships (spouses, parents, children, siblings)
- `photos/` - 70 person photos (jpeg files like image1.jpeg, image22.jpeg etc)

Each person has: key, full_name, first_name, surname, birth, death, profession, photo (filename), spouses[], parents[], children[], siblings[]

## Tech Stack
- DaisyUI + Tailwind CSS (via CDN, NO build step)
- Vanilla JS
- Single HTML file: `index.html`

## Required Features

### 1. Main page - search + person cards
- Header with title "Родовое дерево Шаповаловых"
- Search input (filter by name)
- Grid of person cards using DaisyUI card component:
  - Photo (circular avatar) or placeholder icon if no photo
  - Full name (bold)
  - Birth/death dates
  - Profession badge if exists
  - Click → opens person detail modal

### 2. Person detail modal (DaisyUI modal)
- Large photo or placeholder
- Full info: name, dates, profession
- Relationships sections with clickable links:
  - 💑 Супруг(а): [names as links]
  - 👨‍👩‍👧 Родители: [names as links]  
  - 👫 Братья / Сёстры: [names as links]
  - 👶 Дети: [names as links]
- Clicking a name in modal → opens that person's modal

### 3. Tree view tab (separate view)
- Simple ancestor/descendant tree for selected person
- Use CSS-only tree with DaisyUI styling (no D3 needed)
- Start from Шаповалов Тимофей_1 (key) as default center person
- Show 3 levels: grandparents → parents → person → children
- Boxes styled as DaisyUI cards, connected with CSS lines

### 4. Statistics panel (bottom of main page)
- Total people count
- Number of generations (rough estimate by birth year)
- Number of couples

## Design
- DaisyUI theme: "forest" or "autumn" (warm family feel)
- Language: Russian
- Mobile-friendly
- Smooth modal transitions

## Important
- Photos path: `photos/imageXX.jpeg` (relative path)
- All person keys are used as IDs for navigation
- Handle missing photos gracefully (show avatar placeholder)
- When clicking person name in modal, smooth transition to that person

## Output
Single file `index.html` that works by opening in browser (no server needed for basic functionality, photos need local server or embed).

Also create `README.md` with:
- What this is
- How to use (open index.html, or serve locally)
- GitHub Pages deployment note

When completely done, run:
openclaw system event --text "Done: Family tree website built in /tmp/family-tree-site/" --mode now
