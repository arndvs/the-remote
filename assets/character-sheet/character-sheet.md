# Character Sheet Method — AI Video Reference Images

## Overview

AI video tools like Seedance 2.0 allow you to insert a specific person into generated video. A single photo produces inconsistent results because the model only sees one angle. A **character sheet** — a multi-angle reference board — gives the model enough visual data to maintain consistency across scenes.

## Tools

| Tool | Purpose |
|---|---|
| **Nano Banana Pro** | Generate the character sheet (multi-angle reference image) |
| **Seedance 2.0** | Generate AI video using the character sheet as a reference image |

## Step 1 — Build the Character Sheet

Use the following prompt structure in Nano Banana:

### Layout

- **Background:** White. Clean. Minimalist.
- **Left side:** Full body front view. Side view. Back view. Same character, same clothes, same height.
- **Upper right:** 6 head angle shots — front, side, back, 3/4 view, top down, profile.
- **Lower right:** 6 close-up detail shots — fabric, shoes, eyes, skin, hip, lower body.

### Style

- Professional character design sheet (game art / fashion reference board aesthetic)
- Flat studio lighting, sharp edges, natural hair
- No dramatic lighting, no fancy backgrounds

### Why This Structure Works

The multi-angle layout gives the AI model consistent reference data for face, body proportions, clothing, and texture from every direction. A single photo forces the model to guess what the other angles look like. The character sheet removes the guesswork.

## Step 2 — Load into Seedance 2.0

Upload the completed character sheet as the **reference image** in Seedance 2.0. The model reads the sheet and extracts the character from the multi-angle views.

### Result

- Character stays consistent across scenes because the reference is consistent
- No studio, camera, or crew required
- Build the sheet once, reuse it across any video prompt

## Key Principle

**Consistency is the whole game with AI video.** One photo gives the model one angle. A character sheet gives it everything. Build the sheet first, then build the video.