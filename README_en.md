<p align="center"><img src="media/portada.jpg" alt="Embers Remain" width="900"></p>

<p align="center"><a href="README.md">Español</a> · <b>English</b></p>

# Embers Remain

**Valdren, year 312 of the Flame.** Maelis returns to the heath where the pyres burned. A dark exploration and
combat RPG with an ink-illustration look, made in **Godot 4**.

**Status:** the first chapter (Act I) is playable from start to finish. Version 1.0 will include all three acts.

<p align="center"><img src="media/brezal_dia.png" alt="Brezal by day" width="880"></p>

## The game

- **Real-time melee combat:** slash, thrust and kick combo, heavy attack, dodge, block and counter. Every enemy
  attacks and falls in its own way, and bosses have their own phases.
- **A living village:** day and night, weather, quests that change the place, multi-floor interiors, fishing and
  forging.
- **Interface:** floating prompts with the available action ([E] Talk, Climb, Read…), quest and item
  notifications, and finished quests struck through in the inventory.

| By day | By night |
|---|---|
| <img src="media/brezal_dia.png" width="430"> | <img src="media/brezal_noche.png" width="430"> |
| **Multi-floor interiors** | **Combat** |
| <img src="media/interior.png" width="430"> | <img src="media/combate.png" width="430"> |

<p align="center"><img src="media/mochila.png" alt="Inventory and quests" width="720"></p>

## How it was made: human script, AI art and animation

Embers Remain is also an experiment: **how far can you go drawing and animating a whole game with AI when a
person writes the story, the characters and the design?** Everything runs locally on a single PC.

1. **Characters.** Each character is drawn from the script, front view first (FLUX.2 Klein). Only once it is
   approved does the same model, in edit mode, produce the back and side views from that image, so the design
   stays the same.
2. **3D skeleton.** The three views become a T-pose model (Hunyuan3D-2mv + Blender), animated with Mixamo.
3. **Guides.** Blender renders each animation from the game's three cameras as depth and skeleton videos.
4. **Animation.** Wan 2.1 VACE 14B takes the guide and the character image and draws the animation frame by frame.
5. **Review.** Every batch is watched on video; what fails is redone. Approved frames are cut out and go into Godot.

<p align="center"><img src="media/lamina_maelis.png" alt="Maelis: from reference to game" width="880"></p>
<p align="center"><img src="media/lamina_casas.png" alt="Brezal buildings" width="880"></p>
<p align="center"><img src="media/lamina_noche.png" alt="Buildings by day and by night" width="880"></p>

**Videos:** [trailer](media/embers_remain_trailer.mp4) · [walk and run](media/maelis_caminar_y_correr.mp4) ·
[characters](media/personajes_acto1.mp4)

### What we learned

- AI follows a **shape in the guide** far better than a description in the prompt.
- Asking for the other views **from an already approved image** keeps the design; asking from scratch changes it.
- Human review can't be skipped: a good share of what is generated gets redone at least once.

---

<sub>© 2026 NONA Studio. All rights reserved. The images, art, text, characters and the names "NONA Studio" and
"Embers Remain" are property of NONA Studio.</sub>
