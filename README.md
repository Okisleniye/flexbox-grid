# Assignment #2 — Advanced CSS (Flexbox & Grid)

**Name:** Fariddin
**Group:** 4

## Overview

This project demonstrates advanced CSS layout techniques using Flexbox
and CSS Grid, covering navigation bars, card rows, full-page grid
layouts, an image gallery, and a portfolio page that combines both
systems.

## Project Structure

```
├── index.html          # Task 0 (Navbar) + Task 1 (Card Row)
├── grid-layout.html    # Task 2 (Grid page layout with areas)
├── gallery.html        # Task 3 (Image gallery)
├── portfolio.html      # Task 4 (Flexbox + Grid combined)
├── css/
│   └── style.css       # All styles for every page
├── images/             # Card, gallery, and portfolio graphics
└── screenshots/        # Screenshots referenced in this README
```

## Part 1 — Flexbox

### Task 0. Navigation Bar

A `.navbar` flex container holds the logo on the left and the nav
links on the right using `justify-content: space-between`, with
`align-items: center` to vertically center everything. The links list
is itself a flex container with `gap` for spacing.


### Task 1. Card Row

Three cards inside a `.card-row` flex container (`flex-wrap: wrap`,
consistent `gap`). Each card is a flex column so the image, title,
text, and button stack correctly, with `flex: 1` on the text so
buttons always align to the bottom — giving all cards equal height.
A hover effect lifts the card with `transform: translateY()` and adds
a shadow.

**Screenshot:**

<img width="1920" height="1140" alt="Снимок экрана 2026-09-27 205708" src="https://github.com/user-attachments/assets/4514cf71-9cd3-4bf4-8ec6-968e76206a7f" />

## Part 2 — Grid System

### Task 2. Page Layout with Grid Areas

`.grid-page` is a grid container using `grid-template-areas` to place
a header (spanning the top), a sidebar (left), main content (right),
and a footer (spanning the bottom).

**Screenshot:**

<img width="1920" height="1140" alt="Снимок экрана 2026-09-27 205712" src="https://github.com/user-attachments/assets/554f8eab-82cc-41af-b65c-ba6c52ea63ec" />

### Task 3. Image Gallery

`.gallery` is a 3-column grid (`repeat(3, 1fr)`) with nine items and a
consistent `gap`. Hovering an item fades in a caption overlay
positioned with `position: absolute; inset: 0;`.

**Screenshot:**

<img width="1920" height="1140" alt="Снимок экрана 2026-09-27 205717" src="https://github.com/user-attachments/assets/607af7b6-a65f-4bb7-84af-825ab7119ef0" />


## Part 3 — Combining Flexbox & Grid

### Task 4. Portfolio Page

The page header/nav uses Flexbox (same navbar as the other pages). The
`.portfolio-main` section is a 2-column CSS Grid (`2fr 1fr`) placing
the projects list on the left and an "About Me" sidebar on the right.
Each `.project-card` inside the projects list is itself a flex
container so its title/description and button align on one row. The
footer spans the full width below.

**Screenshot:**

<img width="1920" height="1140" alt="Снимок экрана 2026-09-27 210210" src="https://github.com/user-attachments/assets/400090ff-a56f-4d31-9264-54bf03d4cd6a" />


## Summary of Work Process


I started by separating the layout problems into the two tools they fit
best: Flexbox for one-dimensional arrangements (the navbar, the card
row, and the inside of each project card) and CSS Grid for
two-dimensional layouts (the full-page header/sidebar/main/footer
structure, the image gallery, and the projects-plus-sidebar section of
the portfolio page). The trickiest part was getting the cards in the
card row to have equal height regardless of text length — I fixed this
by making each card a flex column and setting `flex: 1` on the
description text, which pushes every button down to the same baseline.
For the gallery, the hover caption uses `position: absolute; inset: 0`
on top of the image with `opacity` transitioning on `:hover`, which was
simpler than trying to animate a background overlay directly. Building
the portfolio page last showed me clearly how Grid and Flexbox
complement each other: Grid handled the big two-column split, while
Flexbox handled alignment inside each smaller piece (the navbar links
and each project row). Overall the biggest lesson was recognizing when
a layout is fundamentally one axis (use Flexbox) versus when it truly
needs rows and columns together (use Grid).

## Resources Used

- Abitova G.A., *Web Technologies Front-End Development, Part 1* (2022)
- https://www.w3schools.com/css/css3_flexbox.asp
- https://www.w3schools.com/css/css_grid.asp
