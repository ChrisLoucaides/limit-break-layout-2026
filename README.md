# VGBC Style Overlay Properties:
- Forked from: https://github.com/joaorb64/TournamentStreamHelper
- The top left container displays the name of the tournament and the bottom containers each display the player's Twitter handle.
- The match is shown at the bottom of the left player container.
- The phase and best of x is shown at the bottom of the right player container in "phase - best of x" format.
  - If only best of x is available, then only best of x is shown.
  - If it is best of 0 and the phase is available, then only the phase is shown.
- No information alternation takes place in this overlay. 
- Select "Shutdown source when not visible" in the Browser's properties so that it plays the overlay animation every time it becomes visible.

# Limit Break Skin:

- The overlay is skinned to the LIMIT BREAK brand (Electric Cyan `#00D4FF` -> Neon Magenta `#EE00CC` on Deep Navy) so it matches the `versus_screen_webcams` layout.
- Player 1 is always cyan and player 2 always magenta. The per-team colours TSH sends are deliberately ignored, so the pair always reads as the brand.
- All colours live in the `:root` block at the top of `index.css` — edit `--p1` / `--p2` (and their `-deep` / `-glow` partners) to reskin.
- Type is the bundled `var(--font)` (Saira Condensed), which stands in for the brand display face (Barlow Condensed) and carries the CJK fallback needed for player tags. To use Barlow Condensed, load it and put it in front of `var(--font)` in the `body` rule.
- `index.html` has no doctype on purpose: `index.js` uppercases the whole player-name HTML string, so quirks mode is what keeps `class="SPONSOR"` matching the stylesheet.

# Player Cams:

- Included in the scoreboard_vgbootcampy file are the CameraBorders.png and CameraMask.png.
- Add /layout/scoreboard_vgbootcampy/CameraBorders.png as an Image in OBS to set the camera borders.
  - Change the color of the border by adding a Color Correction filter and changing the Color Multiply to your color of choice (cyan `#00D4FF` for player 1, magenta `#EE00CC` for player 2 to match the skin).
- Add an Image Mask/Blend filter to the player cam (1280x720) and select /layout/scoreboard_vgbootcampy/CameraMask.png as its path to round the corners of the player cam.
- Adjust the size of the player cams and move them so they fit nicely within their borders.

# Enjoy!

- You can edit the HTML, CSS, and JavaScript files to change the color and position of words and containers, add your own logo, change animation speed, etc.
