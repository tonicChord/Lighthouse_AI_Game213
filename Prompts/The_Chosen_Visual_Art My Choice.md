-For HUD or UI design, skip this part hence it is next week's topic to cover.

## Step 1: Choose Your Core Art Style (Pick One)


| **Option B: Crisp Illustrated Vector / Sea-Chart** | *Mini Metro*, *Bad North*, *FTL* | Clean, sharp geometric silhouettes with bold outlines 
and antique brass nautical chart lines. | Highest possible gameplay clarity at any zoom level; easiest to generate programmatically as crisp `.svg` / `.png` 
sprites. |

I want readibilty for now. Additionally, increase the overall brightness of the game for playability.


## Step 2: The Master Color Palette (Functional Color Coding)

---Your recommendetion for color palet looks good.

### 1. The Environment (60% of the Screen — Cold, Dark, Receding)
The ocean and storm must stay in deep, desaturated cool tones so that ships, hazards, and light beams pop effortlessly on top of them.
* **Abyssal Midnight (Deep Water Base):** `#030914`
* **Trench Navy (Mid-Water Swells):** `#07162C`
* **Storm Slate (Wave Crests & Rain):** `#1E293B`
* **Lightning Squall Flash (Sky Tint):** `#93C5FD` (at $20\%$–$30\%$ opacity)

### 2. Player Light, UI & Safe Sanctuary (30% — Warm Brass & Safe Teal)
* **Fresnel Beam Core (Active Spotlight):** `#FEF08A` (Warm Ivory-Yellow)
* **Weathered Brass (UI Frames & Reticle):** `#F59E0B` (Rich Amber Gold)
* **Harbor Sanctuary Glow (Safe Zone & Locked Course):** `#2DD4BF` (Bioluminescent Seafoam Teal)
* **Sea-Glass Panel Fill (Transparent HUD):** `#040C18` at $22\%$ opacity

### 3. Threats & Entities (10% — High-Contrast Signal Colors)
* **Friendly Cargo Ships:** Warm Cedar/Oak (`#92400E`), Cream Canvas Sails (`#FEF3C7`), and a **Teal/Gold Prow Lantern** (`#2DD4BF` / `#FDE047`).
* **Pirate Raiders (Cannon Targets):** Charred Pitch-Black Hulls (`#18181B`) with **Blood Crimson Sails** (`#DC2626`) and an Orange Deck Brazier (`#F97316`).
* **Kraken Monsters (Light-Repel Targets):** Deep Eldritch Violet (`#7E22CE`), Bioluminescent Magenta Suckers (`#D8B4FE`), and **Venom Green Eyes** (`#4ADE80`).
* **Static Hazards (Rocks & Whirlpools):** Cold Basalt Grey (`#475569`) surrounded by **Bright Crashing Seafoam White** (`#E0F2FE`) 
so the edge of the hazard is unmistakable.


---Cover the steps from  3 to 5 as you recommended.
---About typography, use IM Fell English SC for display and headers and Cinzel for the rest.

For step 6, I choose option 2. Provide the required prompt for OpenAI's Dall-E. I will generate the required assets with its desktop application.