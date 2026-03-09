# E-R Diagram Generator

> A zero-dependency, browser-only ER diagram editor powered by [Mermaid.js](https://mermaid.js.org/) — just open `index.html` and start designing.

![Demo](docs/demo.gif)

## Features

- **Live rendering** — edit Mermaid `erDiagram` syntax and hit `Ctrl+Enter` (or click Render) to instantly visualize
- **Draggable entities** — grab any entity node and reposition it; relationship lines and labels follow automatically with smart 4-side routing
- **5 built-in templates** — Supply Chain, Hospital, School, E-commerce, and a blank starter
- **SVG export** — download a clean, scalable SVG of your diagram
- **Zoom controls** — zoom in / out / reset the preview
- **Zero install** — single `index.html` file, no build step, no server required
- **Cardinality reference** — always-visible quick reference for Mermaid cardinality notation

## Screenshots

### Supply Chain
![Supply Chain](docs/screenshot-supply.png)

### E-commerce
![E-commerce](docs/screenshot-ecommerce.png)

### Hospital
![Hospital](docs/screenshot-hospital.png)

## Getting Started

### Option 1 — Open directly (simplest)
```
double-click index.html
```
Works offline, no server needed.

### Option 2 — Local HTTP server
```bash
# Python
python -m http.server 8080

# Node.js (npx)
npx serve .
```
Then open `http://localhost:8080` in your browser.

## Usage

1. **Select a template** from the toolbar or start from "Blank"
2. **Edit the syntax** in the left panel — standard Mermaid `erDiagram` format
3. **Press `Ctrl+Enter`** (or click the Render button) to update the preview
4. **Drag entities** in the preview to rearrange the layout
5. **Export SVG** via the button in the top-right of the preview panel

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + Enter` | Render diagram |
| `Tab` | Insert 4-space indent in editor |

## Mermaid erDiagram Syntax Quick Reference

```
erDiagram
    ENTITY_A ||--o{ ENTITY_B : "relationship label"
    ENTITY_A {
        string ID PK
        string Name
        date Created
    }
```

**Cardinality:**

| Symbol | Meaning |
|---|---|
| `\|\|` | Exactly one |
| `o\|` | Zero or one |
| `\|{` | One or more |
| `o{` | Zero or more |

## Built-in Templates

| Template | Description |
|---|---|
| Supply Chain | Supplier, Customer, Order, Item, Shipment, Product |
| Hospital | Patient, Physician, Outpatient, Resident, Bed |
| School | Student, Course, Professor, Department, Grade |
| E-commerce | User, Order, Product, Cart, Payment, Review, Shipping |
| Blank | Minimal starter with two example entities |

## Tech Stack

- **[Mermaid.js 10.6](https://mermaid.js.org/)** — diagram rendering engine
- **Vanilla JS / CSS** — no frameworks, no bundler
- **JetBrains Mono + Noto Sans SC** — via Google Fonts

## License

MIT
