# Pixel Editor / Sprite Tool — Feature Spec (Organized)

## Overview
A browser-based pixel art editor focused on **fast drawing**, **clean exports**, and **optional animation workflows**. Built around a scalable `<canvas>` renderer with crisp nearest-neighbor zoom.

---

## 1) Core MVP (Must-Have)

### 1.1 Canvas Grid Editor
- [ ] Adjustable grid size (e.g., **8×8 → 128×128**)
- [ ] Zoom in/out
- [ ] **Fit to screen** control
- [ ] Toggle **pixel gridlines** (optional)

### 1.2 Drawing Tools
- [ ] **Pencil** (paint 1 cell)
- [ ] **Eraser** (set transparent)
- [ ] **Fill / Bucket** (flood fill)
- [ ] **Color picker / Eyedropper** (pick color from canvas)

### 1.3 Palette
- [ ] Primary + secondary color (**left/right click**)
- [ ] Swatch-based palette UI
- [ ] Add/remove swatches
- [ ] Recent colors history

### 1.4 Undo / Redo
- [ ] History stack with cap (reasonable: **50–200**)

### 1.5 File Actions (Local Files)
- [ ] New / Clear
- [ ] Save project to **JSON** (download)
- [ ] Load project from **JSON** (upload)

### 1.6 Export & Output (High Value)
#### Export PNG
- [ ] Export PNG
- [ ] Scale multiplier (**1×, 4×, 8×, 16×**) with crisp nearest-neighbor
- [ ] Transparent background option

#### Export Spritesheet
- [ ] Export spritesheet
- [ ] Frames per row
- [ ] Padding
- [ ] Frame size
- [ ] Optional: export individual frames

#### Clipboard + Data Output
- [ ] Copy PNG to clipboard (where supported)
- [ ] Copy data as JSON/text

#### Optional (Popular)
- [ ] Export GIF / APNG
  - [ ] FPS control
  - [ ] Loop toggle

---

## 2) Editing Power Features (Post-MVP)

### 2.1 Selections
- [ ] Rectangular selection
- [ ] Move selection
- [ ] Copy / paste selection
- [ ] Flip selection (H/V)
- [ ] Rotate selection (90°)

### 2.2 Canvas Transforms
- [ ] Flip canvas (H/V)
- [ ] Rotate canvas (90° increments)
- [ ] Resize canvas (crop/expand with anchor)

### 2.3 Mirroring / Symmetry
- [ ] Horizontal mirror draw
- [ ] Vertical mirror draw
- [ ] Quad symmetry (optional)

### 2.4 Onion Skinning (Animation Aid)
- [ ] Show previous/next frame overlays
- [ ] Opacity sliders

---

## 3) Animation System (Optional “Sprite Tool” Vibes)

### 3.1 Timeline
- [ ] Frame timeline UI
  - [ ] Add frame
  - [ ] Duplicate frame
  - [ ] Delete frame
  - [ ] Reorder frames

### 3.2 Timing / Playback
- [ ] Global FPS and/or per-frame duration
- [ ] Play / pause preview
- [ ] Ping-pong playback option

---

## 4) UI / UX Enhancements

### 4.1 Keyboard Shortcuts
- [ ] Tools
  - [ ] **B** = Pencil
  - [ ] **E** = Eraser
  - [ ] **G** = Fill
  - [ ] **I** = Eyedropper
- [ ] History
  - [ ] Ctrl/Cmd + Z = Undo
  - [ ] Ctrl/Cmd + Shift + Z = Redo

### 4.2 Mouse / Touch Support
- [ ] Drag to paint continuously
- [ ] Touch-friendly toolbar sizing

### 4.3 Status Bar
- [ ] Cursor coordinates
- [ ] Active color(s)
- [ ] Current tool
- [ ] Zoom level

### 4.4 Themes / Style
- [ ] Light / Dark theme
- [ ] Pixel-ish UI style toggle

### 4.5 Autosave / Recovery
- [ ] Autosave to **localStorage**
- [ ] “Restore last session” prompt/option

---

## 5) Import & Interop (Optional)

### 5.1 Import Image → Pixelate
- [ ] Load PNG/JPG
- [ ] Resize/downsample to grid size
- [ ] Palette reduction (simple quantization)

### 5.2 Import Palette
- [ ] Import from:
  - [ ] `.gpl` (GIMP)
  - [ ] `.ase` (Adobe) (optional)
  - [ ] Plain hex list

### 5.3 Export Code / Fun Formats
- [ ] Export as 2D array of colors
- [ ] CSS `box-shadow` pixel art export (fun)
- [ ] ASCII / emoji art export (bonus)

---

## 6) Collaboration / Sharing (Optional)

- [ ] Shareable link (encode project in URL or use simple backend)
- [ ] Export “project bundle” (JSON + metadata)
- [ ] Gallery view / saved projects list

---

## 7) Performance & Quality Notes

- [ ] Render via `<canvas>` with nearest-neighbor scaling
- [ ] Efficient state model (typed arrays or flat arrays)
- [ ] Flood fill optimized (queue-based)
- [ ] History diffs (store changed pixels vs full frames) for large grids

---

## 8) Accessibility

- [ ] Full keyboard navigation for palette/tools
- [ ] ARIA labels for controls
- [ ] High-contrast mode
- [ ] Colorblind-friendly palette suggestions (optional)
