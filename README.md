# Personal Portfolio Website

Source for [rishabhjain9196.github.io](https://rishabhjain9196.github.io), a responsive single-page portfolio website.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222222?logo=githubpages&logoColor=white)

![Profile image used by the site](images/profilepic.png)

## Overview

The site is a static page built with HTML, CSS and vanilla JavaScript, and served by GitHub Pages. It has navigation, a profile introduction, an experience timeline, skills, education, mentorship, projects, achievements and contact links.

## Structure

```mermaid
flowchart LR
    Browser["Visitor browser"] --> Page["index.html"]
    Page --> Styles["styles.css"]
    Page --> Icon["favicon.svg"]
    Page --> Image["images/profilepic.png"]
    Config["tailwind.config.js"] --> Page
    Package["package.json"] --> Styles
```

| Path | Purpose |
| --- | --- |
| `index.html` | Main single-page portfolio content, navigation, sections and client-side interaction. |
| `styles.css` | Checked-in stylesheet used by the page. |
| `tailwind.config.js` | Tailwind configuration that scans `index.html` and enables class-based light mode styling. |
| `package.json` | Defines Tailwind build and watch scripts. |
| `favicon.svg` | Site icon. |
| `images/profilepic.png` | Profile image used in the page. |

## Features

- Responsive desktop and mobile navigation.
- Scroll reveal effects using `IntersectionObserver`.
- Sticky navigation styling that changes after scrolling.
- Animated counters for headline numbers.
- Light and dark themes, with the choice saved in `localStorage`.

## Run locally

Open `index.html` directly in a browser, or serve the folder locally:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Build notes

The page uses the committed `styles.css`. The npm scripts build it with Tailwind from `src/input.css`, which is not in the repository, so add that file before rebuilding the stylesheet.
