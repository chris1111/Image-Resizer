[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://github.com/chris1111/Image-Resizer/blob/main/LICENSE) [![pages-build-deployment](https://github.com/chris1111/Image-Resizer/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/chris1111/Image-Resizer/actions/workflows/pages/pages-build-deployment)

# Image Resizer

## Start using ➢ [Image-Resizer](https://chris1111.github.io/Image-Resizer/)

### Combined with this tools ➥ [Icon-Studio](https://chris1111.github.io/Icon-Studio/) 
they are the perfect tools for creating themes icons for OpenCore or Clover.

----------------------------------------------------------------------------

### How it work
1. Local & Private (Browser-side)
Everything happens directly inside your web browser using the HTML5 Canvas API. Just like the macOS sips command runs in your terminal, this tool runs in your browser engine. No images are ever uploaded to a server, ensuring 100% privacy.

2. Multiple Drag & Drop
You can drag and drop multiple images (PNG, JPEG, WebP) at once, or click to browse and select them. The tool instantly reads their original dimensions and file sizes.

3. Individual Resize Cards
Instead of forcing one size for all images, the script generates a dedicated "Resize Card" for every image you drop. Each card displays:
	•	The image thumbnail and its original filename.
	•	Separate Width and Height input boxes.
	•	Its own Aspect Ratio Lock checkbox (if locked, changing the width automatically calculates the correct height, and vice versa).

4. The Resizing Process (Canvas API)
When you click "Resize & Download" on a specific card:
	1	The browser creates a hidden <canvas> element of the exact width and height you typed.
	2	It draws your image onto that canvas using high-quality smoothing algorithms to ensure the resized image looks sharp.
	3	It converts the canvas back into an image file (matching the original format).

5. Instant Download
The newly resized image is packaged into a downloadable file automatically. The new file is named with its new dimensions (e.g., myimage-800x600.png) and saved straight to your Downloads folder.

### Updated 15 August 2026

✨ New Visual Effects (On Image Upload)
	1	Horizontal Shooting Star: A bright, skewed light streak now sweeps across the entire width of each image card when it uploads.
	2	Particle Burst: A JavaScript-generated explosion of 14 glowing golden sparks shoots outward from the center of the card.
	3	Expanding Ring & Flash: A glowing border ring expands and fades, paired with a quick radial flash of light (using mix-blend-mode: screen) to simulate a cosmic "spawn."
	4	Upgraded Card Entrance: Replaced the simple fade-up with a smoother animation that includes a slight scale-up and a brightness flash.

⚙️ Logic & Performance Fixes
	5	Fixed Multiple Uploads: Originally, the code rebuilt the entire grid every time a new image loaded, which erased the animation of the first images if you uploaded 10 at once. We changed this to append new cards directly to the bottom, ensuring every single image gets to play its full animation.
	6	Smart Z-Indexing: Carefully layered the shooting star and flashes in front of the card content, but behind the inputs and buttons, so the UI remains fully clickable while the magic happens on top.

🗑️ New UI Features
	7	Individual Remove Button: Added a small X button to the top-right corner of every card.
	8	Smooth Removal Animation: Clicking the remove button triggers a smooth fade-out and scale-down before deleting the card from the DOM.
	9	Dynamic Counter & Auto-Hide: Created an updateCounter() function that instantly updates the "Images Loaded" text when you delete an image, and automatically hides the "Clear All" bar when the list reaches zero.


