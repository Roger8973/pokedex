# 🔴 Pokédex

A Pokédex web application built with **Angular 16**, **TypeScript** and **SCSS**, organized into feature and shared modules with lazy-loaded routing.

> 🚧 **Work in progress** — the layout and component structure are in place (header, search bar and Pokémon cards). Integration with [PokéAPI](https://pokeapi.co/) and the details page are next.

---

## ✨ Features

- **Header** with the Pokédex logo.
- **Search bar** to look up Pokémon by name *(UI only for now)*.
- **Pokémon cards** showing name, types and image *(static data for now)*.
- **Details page** at `/details` *(scaffolded)*.
- **Theme with CSS custom properties** and a SCSS reset, plus a `rem` conversion helper.

## 🛠️ Tech Stack

| Area | Technology |
|---|---|
| Framework | Angular 16 (NgModules) |
| Language | TypeScript 5.1 |
| Styles | SCSS |
| Reactive programming | RxJS 7 |
| Tests | Jasmine + Karma |

## 🧱 Project Structure

```
src/
├── app/
│   ├── pages/                  # Feature module (lazy-loaded)
│   │   ├── home/               # Home page: header + search + list
│   │   ├── details/            # Pokémon details page
│   │   ├── pages.module.ts
│   │   └── routing.module.ts   # Routes: '' → Home, 'details' → Details
│   ├── shared/                 # Reusable components
│   │   ├── poke-header/        # <poke-header>
│   │   ├── poke-search/        # <poke-search>
│   │   ├── poke-list/          # <poke-list>
│   │   └── shared.module.ts
│   ├── app-routing.module.ts
│   └── app.module.ts
├── assets/                     # Icons, background and images
├── config-scss/                # variables.scss, reset.scss, rem-cal.scss
└── styles.scss                 # Global styles
```

### Routes

| Route | Page |
|---|---|
| `/` | Home — Pokémon list and search |
| `/details` | Pokémon details |

### Color palette

| Variable | Color |
|---|---|
| `--primary-color` | `#262835` |
| `--secondary-color` | `#FF5473` |
| `--cinza` | `#EFEFEF` |
| `--branco` | `#FFFFFF` |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 16.14+ or 18.10+ (required by Angular 16)
- npm

### Steps

```bash
git clone https://github.com/Roger8973/pokedex.git
cd pokedex
npm install
npm start
```

Open `http://localhost:4200/`. The app reloads automatically when you change a source file.

### Available scripts

| Command | Description |
|---|---|
| `npm start` | Starts the dev server (`ng serve`) |
| `npm run build` | Production build in `dist/` |
| `npm run watch` | Development build in watch mode |
| `npm test` | Runs unit tests with Karma |

## 📌 Roadmap

- [ ] Service to fetch Pokémon from [PokéAPI](https://pokeapi.co/) with `HttpClient`
- [ ] Render the list dynamically from the API
- [ ] Search/filter by name
- [ ] Details page with stats, abilities and evolutions (route with `:id`)
- [ ] Pagination or infinite scroll
- [ ] Type-based card colors
- [ ] Responsive layout
- [ ] Upgrade to the latest Angular version

## 👤 Author

**Roger Fraga Messina** — [GitHub](https://github.com/Roger8973)
