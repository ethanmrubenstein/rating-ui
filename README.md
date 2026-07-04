# Rating UI

An interactive star rating component built with React and Vite. Users hover and click to select a rating, see a live feedback message for their selection, and submit to get a thank-you confirmation modal.

## Features

- **Interactive stars** — hover previews and click to set a 1–5 star rating
- **Live feedback** — a customizable message reflects the currently selected rating
- **Submit + confirmation** — a Submit button (disabled until a rating is chosen) opens a thank-you modal
- **Configurable** — customize the heading, star color, and per-rating feedback messages via props

## Components

- [`Rating`](src/components/Rating.jsx) — the main component; manages rating/hover/submitted state and composes the others
- [`Star`](src/components/Star.jsx) — a single star that handles click and hover interactions
- [`Modal`](src/components/Modal.jsx) — the thank-you confirmation dialog shown after submitting
- [`Button`](src/components/Button.jsx) — a reusable button used by the rating and modal

## Props

The `Rating` component accepts the following props:

| Prop               | Type       | Default                                             | Description                     |
| ------------------ | ---------- | --------------------------------------------------- | ------------------------------- |
| `heading`          | `string`   | `"Rate Your Experience"`                            | Heading shown above the stars   |
| `color`            | `string`   | `"gold"`                                            | Color of selected/hovered stars |
| `feedbackMessages` | `string[]` | `["Terrible", "Poor", "Fair", "Good", "Excellent"]` | Messages shown for ratings 1–5  |

### Example

```jsx
import Rating from "./components/Rating";

<Rating
  heading="How do you feel about React?"
  feedbackMessages={["Hate it", "Dislike it", "Meh", "Like it", "Love it"]}
/>;
```

## Getting Started

```bash
npm install
npm run dev
```

## Scripts

- `npm run dev` — start the Vite dev server with HMR
- `npm run build` — build for production
- `npm run preview` — preview the production build
- `npm run lint` — run ESLint

## Tech Stack

- [React 19](https://react.dev)
- [Vite](https://vite.dev)
- [ESLint](https://eslint.org)
