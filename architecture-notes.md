GIT 414 - Deliverable 2 - CSS Architecture Notes
Project: Desert After Dark

This is the first CSS setup for my Desert After Dark website. I'm not building the full site yet. The HTML placeholder page is just a way to show how the styles work before I start to build and finalize the rest of the pages.


Organization:
I kept everything in one stylesheet since the project is still small. The layers are ordered as reset, base, layout, components, utilities, states, overrides, and print. That gives each part of the CSS a purpose. For example, general text styles go in base, the card grid goes in layout, and the individual card styles go in components. I'm not using the overrides layer yet, but it's there if I need it later. I've also tried to keep the selectors simple rather than using !important.


Colors and other values:
The colors are from the Desert After Dark palette I chose. Deep Night is the main background, Dusk Surface is for cards, and Rock Umber is used for the photo placeholders. Orange is for buttons, pink is for animal category tags, green is for the fun-fact box, and sand is for links and focus outlines. I added light text colors so the page is readable against the dark background.

The font, font sizes, spacing, and rounded corners are starting values and not the final design choices. I used Arial for now because it's simple and doesn't require loading a font. The spacing values give me a consistent place to start. I'll probably change some of these as I work on the actual pages. Having them as custom properties should make that easier. I also used a couple of properties just for the button and fun-fact components.


Components and interactions:
The sample shows navigation, buttons, animal cards, a fun-fact box, and a footer. I used class names based on what they do, plus three small u- utility classes. The animal cards go from one column on mobile to two on medium screens and three on wider screens. I also decided to leave the hero open instead of putting it in another card.

I added hover, keyboard focus, current-page, and pressed-button styles. For printing, the CSS hides the navigation and empty photo placeholders and switches to a simpler layout with dark text on white.


What I simplified:
Before: My earlier draft included a separate patterns.html page and CSS for animal profile and adaptation layouts that I haven't built yet.

After: I removed those extras and kept one .animal-grid with reusable .animal-card styles. Shared colors and spacing use custom properties instead of repeating the same values. I think this makes more sense for an assignment focused on the CSS structure rather than a finished website.


Testing:
The preview was checked in Chromium and Firefox at 320px, 375px, 768px, and 1280px. There was no horizontal scrolling in those checks, and the card columns adjusted as intended. Focus, current-page styling, and print-media rules were also checked in Chromium.

I still need to test the actual Print Preview. The animal content, photos, and remaining pages will come later.
