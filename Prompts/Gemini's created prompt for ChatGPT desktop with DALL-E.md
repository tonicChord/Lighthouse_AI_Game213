# Beacon of the Storm — Locked Visual Art Direction & DALL-E Prompt Book

*(Note: All HUD and UI design elements have been omitted and reserved for next week's milestone.)*

---

## Step 1: Locked Core Art Style — Crisp Illustrated Vector / Sea-Chart

* **Visual Reference Games:** *Bad North*, *FTL: Faster Than Light*, *Mini Metro*, *Return of the Obra Dinn* (map view).
* **Look & Feel:** Clean, razor-sharp geometric silhouettes with bold dark ink outlines, flat vector shading, and antique brass nautical chart linework.
* **Playability Brightness Adjustment (Moonlit Sea-Chart Mode):**
  * Instead of pitch-black darkness that hides the map, the game uses **High-Visibility Moonlit Chart Lighting**.
  * The unlit ocean remains clearly visible at all times (darkness overlay capped at $45\%$–$50\%$ opacity instead of $85\%$), allowing players to read rock formations, whirlpool currents, and approaching silhouettes across the entire screen while the lighthouse beam acts as a high-contrast golden activation zone.

---

## Step 2: The Master Color Palette (High-Readability Edition)

We use a strict **60-30-10 Functional Color Rule** where every color signals gameplay behavior immediately:

### 1. The Environment (60% of the Screen — Moonlit Nautical Chart)
Cool, high-clarity navy and slate tones with boosted baseline brightness so ships and hazards are always legible even outside the spotlight:
* **Abyssal Midnight (Deep Water Base):** `#030914` *(boosted in-engine with moonlit ambient fill to `#0B192C`)*
* **Trench Navy (Mid-Water Swells & Chart Grid):** `#07162C` *(brightened crest lines at `#16325B`)*
* **Storm Slate (Wave Crests & Rain):** `#1E293B`
* **Lightning Squall Flash (Sky Tint):** `#93C5FD` (at $20\%$–$30\%$ opacity)

### 2. Player Light & Safe Sanctuary (30% — Warm Brass & Safe Teal)
* **Fresnel Beam Core (Active Spotlight):** `#FEF08A` (Warm Ivory-Yellow)
* **Weathered Brass (Beacon Tower & Chart Accents):** `#F59E0B` (Rich Amber Gold)
* **Harbor Sanctuary Glow (Safe Zone & Locked Course):** `#2DD4BF` (Bioluminescent Seafoam Teal)

### 3. Threats & Entities (10% — High-Contrast Signal Colors)
* **Friendly Cargo Ships:** Warm Cedar/Oak (`#92400E`), Cream Canvas Sails (`#FEF3C7`), and a **Teal/Gold Prow Lantern** (`#2DD4BF` / `#FDE047`).
* **Pirate Raiders (Cannon Targets):** Charred Pitch-Black Hulls (`#18181B`) with **Blood Crimson Sails** (`#DC2626`) and an Orange Deck Brazier (`#F97316`).
* **Kraken Monsters (Light-Repel Targets):** Deep Eldritch Violet (`#7E22CE`), Bioluminescent Magenta Suckers (`#D8B4FE`), and **Venom Green Eyes** (`#4ADE80`).
* **Static Hazards (Rocks & Whirlpools):** Cold Basalt Grey (`#475569`) surrounded by **Bright Crashing Seafoam White** (`#E0F2FE`) so the collision edge is unmistakable.

---

## Step 3: Game Object Design Blueprints (2D Top-Down Vector Sprites)

### The Golden Technical Rule for 2D Sprites
Every moving ship sprite is designed from a **strict $90^\circ$ top-down overhead view**, facing **East / Right ($0^\circ$)** on an isolated background. This allows the game engine to rotate a single sprite smoothly across all $360^\circ$ to match your `lastLightDir` vector.

### 1. Friendly Cargo Ships (3 Distinct Silhouettes)
* **Class 1: Swift Cutter (Fast / Agile)**
  * **Target Game Size:** $128 \times 96\text{ px}$
  * **Visual Silhouette:** Narrow, teardrop racing hull with a long front bowsprit pole, light teak wood deck, **1 billowing cream sail** (`#FEF3C7`), and a bright seafoam-teal stripe (`#2DD4BF`) along the gunwale.
* **Class 2: Merchant Brig (Balanced Hauler)**
  * **Target Game Size:** $128 \times 96\text{ px}$
  * **Visual Silhouette:** Medium-width rounded oak hull (`#92400E`) with a raised stern cabin, wooden cargo crates lashed to the center hatch, and **2 cream-gold sails** (fore and main mast).
* **Class 3: Heavy Galleon (Slow / High-Value Treasure Ship)**
  * **Target Game Size:** $144 \times 108\text{ px}$
  * **Visual Silhouette:** Wide, imposing fortress-like mahogany hull with gold-trimmed stern quarters (`#F59E0B`), emerald-teal accents, and **3 wide cream canvas sails**.

### 2. Enemy Designs: Pirate Raider & Kraken
* **Pirate Raider (The Hunter)**
  * **Target Game Size:** $128 \times 96\text{ px}$
  * **Visual Hooks:** Spiked dark-iron front bow ram, scorched pitch-black hull (`#18181B`), **2 jagged blood-crimson sails** (`#DC2626`) with a stark white skull emblem, and a glowing orange fire brazier (`#F97316`) on the bow deck.
* **The Kraken (The Abyssal Lurker)**
  * **Target Game Size:** $160 \times 160\text{ px}$
  * **Visual Hooks:** Central royal-violet cephalopod mantle (`#7E22CE`) with two glowing venom-green eyes (`#4ADE80`), surrounded by **8 symmetrical curling tentacles** lined with glowing magenta suckers (`#D8B4FE`).

### 3. Static Hazards & Landmarks
* **Jagged Basalt Rocks:** Sharp, faceted slate-grey geometric rock cluster (`#475569`) ringed by a bold white seafoam collar (`#E0F2FE`) and a turquoise shallow-reef outline (`#2DD4BF`).
* **Abyssal Whirlpool:** Circular spinning maelstrom (`256 \times 256\text{ px}$) with a pitch-black center eye and four crisp spiral arms of cyan and white seafoam (`#E0F2FE`).
* **The Lighthouse Promontory & Safe Harbor Ring:** Circular granite cliff island with a red-and-white spiral masonry tower and golden brass Fresnel lens dome (`#F59E0B`), paired with a circular curved wooden breakwater cove lit by teal lanterns (`#2DD4BF`).

---

## Step 4: Typography System (In-World & Display)

To establish an authentic 19th-century nautical sea-chart identity, the project uses this two-font pairing (both free on Google Fonts):

1. **Display Titles & Dramatic Callouts (`IM Fell English SC`):**
   * Used for game titles, major event banners, and dramatic world callouts (`DOCKED!`, `CORSAIR SUNK!`, `KRAKEN REPELLED!`). Delivers an authentic historic engraved maritime print feel.
2. **Secondary Text & Labels (`Cinzel`):**
   * Used for all remaining text, ship class tags (`SWIFT CUTTER`, `HEAVY GALLEON`), and world annotations. Crisp, high-contrast serif proportions that stay readable at any scale.

---

## Step 5: Textures & Atmospheric Overlays

To make the 2D screen look like a living, well-lit nautical chart, we use two seamless tile textures:
1. **`ocean_tile_512.png` ($512 \times 512\text{ px}$ Seamless Tile):** Brightened trench-navy water (`#0B192C`) with crisp, stylized geometric wave crest lines (`#1E293B`) and subtle brass chart grid markings.
2. **`foam_caustics_512.png` ($512 \times 512\text{ px}$ Seamless Overlay):** Clean vector water ripples and light seafoam flecks (`#E0F2FE`) that scroll with the storm crosswind to make wind direction visually obvious.

---

## Step 6: OpenAI DALL-E Prompt Book (For ChatGPT Desktop App)

### Non-Designer Tips for Generating Game Sprites in DALL-E
1. **Use $1024 \times 1024$ Square Format:** By default, DALL-E in the ChatGPT desktop app generates $1024 \times 1024\text{ px}$ square images, which is ideal for rotatable top-down game sprites.
2. **Why Every Prompt Specifies a "Solid Pure White `#FFFFFF` Background":** DALL-E cannot export true transparent `.png` files directly—if you ask for "transparent background," it will draw a fake grey-and-white checkerboard pattern into the image! Asking for a **solid flat pure white background (`#FFFFFF`) with no drop shadows** makes it effortless to remove the background in 1 click (or you can ask ChatGPT right in the same chat: *"Use Python to remove the white background and make it a transparent PNG facing right"*).
3. **Orientation Check:** After generating a ship, make sure its bow (front) points **East / Right ($0^\circ$)**. If DALL-E draws it pointing up, simply ask ChatGPT: *"Rotate this image 90 degrees clockwise so the ship faces right."*

---

### 1. Friendly Cargo Ship — Class 1: Swift Cutter (`cargo_cutter.png`)
```text
Flat 2D top-down overhead game sprite of a small, fast 18th-century wooden sailing cutter ship, facing strictly to the right (East). Crisp illustrated vector art style inspired by Bad North and FTL, with bold dark ink outlines and clean cel-shaded geometric shapes. Narrow aerodynamic teardrop hull made of warm cedar wood (#92400E) with a bright seafoam-teal accent stripe (#2DD4BF) along the side rails, a long front bowsprit pole pointing right, a glowing golden lantern dot (#FDE047) on the front tip, and exactly ONE billowing cream-white canvas sail (#FEF3C7) in the center. Strict 90-degree bird's-eye overhead view, no perspective tilt. Isolated on a completely flat, solid pure white background (#FFFFFF) with no water, no waves, and no external drop shadow.
```

### 2. Friendly Cargo Ship — Class 2: Merchant Brig (`cargo_brig.png`)
```text
Flat 2D top-down overhead game sprite of a medium 18th-century wooden merchant brig cargo ship, facing strictly to the right (East). Crisp illustrated vector art style inspired by Bad North and FTL, with bold dark ink outlines and clean geometric cel-shading. Medium-width rounded oak hull (#92400E) with visible wooden cargo crates lashed to the middle deck, a raised stern cabin on the left, a glowing teal lantern (#2DD4BF) on the front bow pointing right, and TWO billowing cream-gold canvas sails (#FEF3C7) on fore and main masts. Strict 90-degree bird's-eye overhead view, no perspective tilt. Isolated on a completely flat, solid pure white background (#FFFFFF) with no water, no waves, and no external drop shadow.
```

### 3. Friendly Cargo Ship — Class 3: Heavy Galleon (`cargo_galleon.png`)
```text
Flat 2D top-down overhead game sprite of a large, wide, heavy treasure galleon ship, facing strictly to the right (East). Crisp illustrated vector art style inspired by Bad North and FTL, with bold dark ink outlines and clean geometric vector shading. Wide fortress-like mahogany hull (#92400E) with ornate golden brass trim (#F59E0B) on the rear stern castle, emerald-teal canopy accents (#2DD4BF), a glowing golden lantern on the front bow pointing right, and THREE large billowing cream canvas sails (#FEF3C7). Strict 90-degree bird's-eye overhead view, no perspective tilt. Isolated on a completely flat, solid pure white background (#FFFFFF) with no water, no waves, and no external drop shadow.
```

### 4. Enemy Ship — Pirate Raider (`pirate_raider.png`)
```text
Flat 2D top-down overhead game sprite of a menacing pirate raider warship, facing strictly to the right (East). Crisp illustrated vector art style inspired by Bad North and FTL, with bold dark outlines and sharp geometric shapes. Charred pitch-black wooden hull (#18181B), a jagged dark-iron spiked ram on the front bow pointing right, a glowing orange fire brazier (#F97316) on the front deck, and TWO tattered blood-crimson red sails (#DC2626) with a minimalist white skull emblem visible from above. Strict 90-degree bird's-eye overhead view, no perspective tilt. Isolated on a completely flat, solid pure white background (#FFFFFF) with no water, no waves, and no external drop shadow.
```

### 5. Enemy Monster — The Kraken (`kraken.png`)
```text
Flat 2D top-down overhead game sprite of a stylized sea monster Kraken, viewed from directly above. Crisp illustrated vector art style inspired by Bad North and FTL, with bold dark ink outlines and clean flat geometric shading. Central round cephalopod head/mantle in deep eldritch violet (#7E22CE) with two bright glowing venom-green eyes (#4ADE80), surrounded symmetrically by 8 curling tentacles radiating outward like a starburst, with glowing magenta bioluminescent spots (#D8B4FE) on the tentacles. Strict 90-degree bird's-eye overhead view, centered in frame. Isolated on a completely flat, solid pure white background (#FFFFFF) with no water and no external shadow.
```

### 6. Static Hazard — Jagged Basalt Reef Cluster (`rock_cluster.png`)
```text
Flat 2D top-down overhead game sprite of a dangerous jagged ocean rock reef cluster, viewed from directly above. Crisp illustrated vector art style inspired by Bad North, with bold dark outlines and sharp angular geometric facets. Three overlapping sharp basalt rock crags in cold slate grey (#475569) with crisp light-grey facet highlights, surrounded by a bold ring of bright white crashing seafoam (#E0F2FE) and a thin outer ring of turquoise shallow reef (#2DD4BF). Strict 90-degree bird's-eye overhead view, centered in frame. Isolated on a completely flat, solid pure white background (#FFFFFF) with no external background water.
```

### 7. Static Hazard — Abyssal Whirlpool Vortex (`whirlpool.png`)
```text
Flat 2D top-down overhead game sprite of a circular spinning ocean whirlpool maelstrom, viewed from directly above. Crisp illustrated vector art style inspired by nautical sea charts and Bad North. Pitch-black circular center eye (#030914) transitioning into deep teal-navy (#07162C) with four clean, symmetrical logarithmic spiral arms of bright white and seafoam-cyan froth (#E0F2FE and #2DD4BF). Circular badge-like silhouette that can be rotated smoothly in a 2D game engine. Isolated on a completely flat, solid pure white background (#FFFFFF).
```

### 8. Landmark — The Lighthouse Promontory (`lighthouse_island.png`)
```text
Flat 2D top-down overhead game sprite of a circular rocky lighthouse island, viewed from directly above (90-degree bird's-eye view). Crisp illustrated vector art style inspired by Bad North and antique sea charts, with bold outlines. Circular dark granite cliff island (#475569) edged with a crisp white seafoam ring (#E0F2FE), a circular stone keep base in the center, a red-and-white spiral painted lighthouse roof viewed from directly above, and a glowing golden brass Fresnel lantern dome (#F59E0B and #FEF08A) in the exact center. Isolated on a completely flat, solid pure white background (#FFFFFF).
```

### 9. Landmark — Safe Harbor Breakwater Ring (`safe_harbor.png`)
```text
Flat 2D top-down overhead game sprite of a circular wooden harbor breakwater ring forming a safe cove, viewed from directly above (90-degree bird's-eye view). Crisp illustrated vector art style inspired by Bad North, with bold dark ink outlines. Two curved C-shaped weathered oak wooden piers/jetties (#92400E) forming a protective circle with an open entrance gap on the left, decorated with 8 glowing bioluminescent seafoam-teal and brass lantern buoys (#2DD4BF and #F59E0B) spaced around the perimeter. Inside of the ring and outside background must be solid pure white (#FFFFFF) for easy transparency cutout.
```

### 10. Seamless Texture — Moonlit Nautical Chart Ocean (`ocean_tile_512.png`)
```text
Seamless tileable 2D top-down ocean water texture in a crisp illustrated vector nautical sea-chart style. Readable moonlit trench-navy base color (#0B192C) with clean, stylized geometric wave crest lines in storm slate (#1E293B) and subtle antique brass nautical compass grid lines (#F59E0B at low opacity). High gameplay readability, flat 2D overhead view, full-bleed square texture with no vignette and no borders.
```

---

### Follow-Up Command for ChatGPT Desktop (To Auto-Remove the White Background)
Right after DALL-E generates any sprite above in your ChatGPT desktop app, paste this single line into the chat so ChatGPT's built-in Python tool converts it into a ready-to-use transparent `.png` for you:

> *"Use Python (PIL/numpy) to remove the pure white background from this image (making all near-white background pixels transparent), crop it tightly around the centered sprite with padding, resize it to 256x256 pixels, and give me a downloadable transparent PNG."*