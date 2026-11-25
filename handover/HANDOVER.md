# Handover: bathroom images in Runway

Paste the "Message for the local session" block below into a local Claude session that has Claude in Chrome connected. Everything it needs is in this folder.

## Where things stand

- **Project:** interiors for a ground-floor 3-bedroom house (28' × 67' plot). There is a Three.js walkthrough (`index.html`) and a set of photoreal room images.
- **Primary bathroom (Mom & Dad's): locked.** Final image: `images/primary-bath-locked.jpg`. Layout: `images/primary-bath-plan-9x6.png` (9'-0" × 6'-0").
  - Navy picket feature wall at the shower end, white marble-look walls, terrazzo floor meeting plain warm-white tile on a curved brass inlay, brushed brass fittings, oval backlit mirror.
- **Guest bathroom: in progress.** Layout: `images/guest-bath-plan-6x6.png` (6'-0" × 6'-0", to scale).
  - Shower 2'-6" deep across the duct end behind a fixed glass panel; WC and a small basin side by side on the opposite end wall; sliding door from the guest bedroom next to the basin.
  - Style direction: botanical mural tile on the upper walls, fluted panelling on the lower walls up to the 3'-8" WC ledge, small hexagon mosaic floor. Inspiration: `images/guest-inspo-style.jpg`.
  - Option 1 (Forest Crema mural) has been generated once in Canva, view toward the WC and basin: https://www.canva.com/M/MAHb1O33VKc
  - Still to generate: option 2 (pastel tropical), option 3 (dark botanical), and the shower-side view of the chosen option.
- **Not done in the walkthrough:** the primary bathroom there is still 8 ft long with the old blue finish. The owner has not said which side the extra foot comes from.

## Owner's preferences

- Warm luxury only. Guest room: light and soothing.
- No wood in bathrooms, calm rather than dramatic.
- Floors should have some design to them, not plain.
- Check every result against the plan: earlier Runway attempts moved the WC to the wrong wall.

## Images in `images/`

| File | Use |
|---|---|
| `guest-bath-plan-6x6.png` | Guest bath layout plan |
| `guest-inspo-style.jpg` | Style idea only (mural + fluted + mosaic) |
| `guest-tile-forest-crema.jpg` | Option 1 mural tile (ICON Forest Crema Decor, 60×120 cm matt) |
| `guest-tile-essence-crema.jpg` | Plain cream wall tile (ICON Essence Crema) |
| `guest-tile-pastel-tropical.jpg` | Option 2 mural tile |
| `guest-tile-dark-botanical.jpg` | Option 3 mural tile |
| `primary-bath-locked.jpg` | Locked primary bath, style reference |
| `primary-bath-plan-9x6.png` | Primary bath layout plan |
| `mat-como.jpg`, `mat-white-marble.jpg` | Primary bath navy picket and white wall tiles |

## Message for the local session

```
Open Runway in Chrome (I'm signed in) and generate photoreal images of my guest bathroom using an image model that accepts reference images (Gen-4 Image References or Nano Banana Pro). The reference images are in handover/images/ in this repo. Do one image at a time, show me each result, and check it against the layout plan before moving on. Don't buy credits or change any account settings; stop and tell me if Runway asks for payment.

Run these in order:
1. Option 2, pastel tropical, view toward WC and basin
2. Option 3, dark botanical, view toward WC and basin
3. Option 1, Forest Crema, view toward the shower

Prompts are in handover/HANDOVER.md under "Prompts".
```

## Prompts

### Base prompt (option 1, Forest Crema, view toward WC and basin)

Attach in order: `guest-bath-plan-6x6.png`, `guest-inspo-style.jpg`, `guest-tile-forest-crema.jpg`, `guest-tile-essence-crema.jpg`.

```
Photorealistic interior photograph of a compact luxury guest bathroom, 6 ft long × 6 ft wide, 10 ft ceiling. Follow the floor plan in image 1 exactly. Use image 2 only for the design idea: botanical mural on the upper walls, fluted panelling on the lower walls, mosaic floor. Do not copy its dark colours or its layout.

Camera: standing inside the shower at the far end with your back to the end wall, eye level 5 ft, 14mm wide lens, looking straight down the length of the room at the opposite end wall.

Layout, as seen from the camera:
- FAR END wall: on the left half, a white wall-hung WC facing the camera, with a ledge 3 ft 8 in high behind it hiding the cistern and a brushed brass flush plate. On the right half, beside the WC, a small floating basin unit 24 in wide with a white bowl, a wall-mounted brass tap and a tall oval backlit mirror above.
- RIGHT wall: the doorway from the bedroom next to the basin, with a sliding door slid open.
- LEFT wall: no fixtures, one brass towel rail.
- NEAR FOREGROUND: the edge of a fixed clear frameless glass shower panel on the left.

Materials: lower walls up to 3 ft 8 in are fluted sage green matte tile with a slim brass trim on top, running level with the WC ledge. Upper walls from 3 ft 8 in to the ceiling are the tropical botanical mural tile from image 3, 60×120 cm matte porcelain panels, the pattern continuing across the joints, on the far end wall and the left wall. The remaining walls and the inside of the shower are the plain cream matte tile from image 4. Floor: small hexagon mosaic in a soft mix of cream, sage and warm grey. The basin unit is fluted sage green to match the lower walls.

Mood: light, soothing, warm luxury. Soft warm cove light at the ceiling, glow behind the mirror, one small opal globe pendant beside the mirror. Brushed brass fittings, white towels, one small plant on the ledge. No window, no bathtub, no wall art, no text, no dark walls.

Architectural photography, realistic scale, straight vertical lines, high detail.
```

### Option 2: pastel tropical

Attach `guest-tile-pastel-tropical.jpg` as image 3 instead. In the Materials paragraph:
- "fluted sage green matte tile" becomes "fluted warm greige matte tile" (same for the basin unit)
- the floor becomes "small hexagon mosaic in a soft mix of cream, blush and warm grey"

### Option 3: dark botanical

Attach `guest-tile-dark-botanical.jpg` as image 3 instead. Replace the Materials and Mood paragraphs with:

```
Materials: the far end wall above the 3 ft 8 in ledge is the only mural wall, in the dark charcoal botanical tile from image 3. Lower walls up to 3 ft 8 in are fluted deep olive green matte tile with a slim brass trim. All other walls and the inside of the shower are the plain cream matte tile from image 4, to keep the small room bright. Floor: small hexagon mosaic in cream, olive and charcoal. The basin unit is fluted deep olive.

Mood: moody but warm. Soft warm cove light at the ceiling, glow behind the mirror, one small opal globe pendant. Brushed brass fittings, white WC and basin, white towels, one small plant. No window, no bathtub, no wall art, no text.
```

### Shower-side view (any option)

Replace the Camera and Layout paragraphs with:

```
Camera: standing with your back against the end wall where the WC and basin are, eye level 5 ft, 14mm wide lens, looking straight down the length of the room at the shower end wall.

Layout, as seen from the camera:
- FAR END: a walk-in shower 2 ft 6 in deep across the full 6 ft width. One fixed clear frameless glass panel 3 ft 6 in wide on the right, open walk-in gap 2 ft 6 in wide on the left. Brass rain shower head, brass hand shower, recessed lit niche on the right side wall inside the shower.
- LEFT wall: the doorway from the bedroom with a sliding door, slid open. Nothing else on this wall.
- RIGHT wall: the mural above the fluted lower wall, one brass towel rail.
- NEAR FOREGROUND, bottom edge of frame: the front edge of the white wall-hung WC on the right and the corner of the small floating basin on the left.
```

For this view, also add to Materials: "The shower end wall is tiled floor to ceiling in the mural tile from image 3."

### If the layout comes out wrong

Add as the last line: "Do not change the layout: WC and basin side by side on one end wall, shower across the opposite end, door on the long wall next to the basin."
