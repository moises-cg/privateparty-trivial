# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Trivial FDF — a single-page trivia game about "Festival de Fiestas" (FDF). The entire app lives in one file: `index.html`. No build tools, no dependencies, no framework.

## Architecture

- **Single HTML file** (`index.html`) containing all markup, CSS, and JavaScript inline.
- **Language**: Spanish (UI text, questions, explanations).
- **Three screens**: Welcome → Question → Results, toggled via `.screen.active` CSS class.
- **Question data**: the `questions` array in the `<script>` block. Each entry has `text`, `options`, `correct` (index), `layout` ("two-col" or "four-col"), and `explanation`.
- **Confetti**: canvas-based animation triggered on good results (≥50%).

## Development

Open `index.html` directly in a browser. No server or build step required.

To add a new question, append an object to the `questions` array following the existing format.
