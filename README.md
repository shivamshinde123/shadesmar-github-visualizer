# Shadesmar GitHub Visualizer

A single self-contained HTML file that visualizes a GitHub user's repositories as a Shadesmar-themed 3D scene using Three.js.

Inspired by Shadesmar from Brandon Sanderson's Stormlight Archive — a dark obsidian island floating in a sea of glass beads, with crystalline trees representing repositories and flickering flames representing contributors.

## Detailed Documentation

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/shivamshinde123/shadesmar-github-visualizer)

## Features

### Visual Elements
- **Obsidian Island** — procedural terrain with noise displacement and flat shading
- **Crystal Trees** — one per repository, trunk height proportional to commit count (log scale), blue-purple tint with emissive glow
- **Bead Sea** — 20,000 particles with ocean-like wave animation (rolling waves, cross chop, swell, ripples)
- **Contributor Flames** — floating candle sprites near the island, one per unique contributor
- **Sun** — glowing sphere with inner/outer glow, camera-relative positioning so it's always visible
- **Lighting** — balanced directional, ambient, hemisphere, and fill lights with ACESFilmic tone mapping
- **Fog** — linear fog (60–220) for depth and infinite sea illusion

### Interactions
- Click-drag to orbit, scroll or slider to zoom
- Click a tree: camera tweens to focus, side panel shows repo details (branches, recent commits)
- Click a contributor flame: linked tree highlights in amber
- Hover over flame: shows contributor name tooltip
- Zoom and brightness sliders with icons
- Info button (i) explaining the visualization and its Stormlight Archive inspiration

### GitHub API
- Fetches public repos, contributors, commit counts, branches, and recent commits
- Supports both classic and fine-grained Personal Access Tokens
- Handles HTTP 204/401 gracefully

## Usage

1. Open `index.html` in a modern browser
2. Enter a GitHub username (and optionally a Personal Access Token for higher rate limits)
3. Explore the 3D visualization

## Tech Stack

- Single HTML file, no build step
- Three.js (r128) loaded from CDN
- GitHub REST API
- Google Fonts (Inter)

## Credits

Built by [Shivam Shinde](https://github.com/shivamshinde123)
