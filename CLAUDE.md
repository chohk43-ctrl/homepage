# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static family homepage for a Korean family (조혜경 가족). No build tools, frameworks, or package managers — the entire application is a single `index.html` file.

## Running the Project

Open `index.html` directly in a web browser. There are no build steps, no server required, and no dependencies to install.

## Architecture

All HTML, CSS, and JavaScript live in a single file (`index.html`):

- **Lines 1–478**: HTML structure and embedded CSS
- **Lines 671–870**: Embedded JavaScript

**Sections** (top to bottom): sticky nav → hero → family member cards → history/timeline → interactive calendar → photo gallery → footer.

**State persistence**: Family events are stored in `localStorage` under the key `'family-events'`. Photos are stored as base64 strings in memory only (lost on page refresh).

**Styling conventions**: Color palette uses CSS custom properties; primary accent is `#f4845f`. Korean text uses `Noto Sans KR` (Google Fonts); decorative headings use `Playfair Display`. Mobile breakpoint is `768px`.

## Key Behaviors to Preserve

- Calendar events survive page refresh via `localStorage`.
- Photo uploads are in-memory only — no server-side storage.
- The page is in Korean (`lang="ko"`); keep all user-visible text in Korean.
