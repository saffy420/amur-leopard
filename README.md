# Three Selves, One Species: The Amur Leopard

An interactive web exhibit about phenotypic variation and conservation of the Amur leopard. Built as an AP Biology final project.

## Preview

<!-- Screenshots are worth adding here since the design and interactions are the main point of this project -->
<!-- Add a screenshot of the exhibit interface -->
![Project preview](assets/preview.png)

## Why I Built This

For my AP Biology final project I wanted to do something that actually showed biological concepts rather than just describing them. Amur leopards are critically endangered with only around 120 adults left, and the biology of why that matters comes down to genetic diversity. I wanted to make that tangible in a way a poster or slideshow could not.

The project ended up being as much about design as it was about biology. I wanted it to feel like a real museum exhibit rather than a school project website, so I spent a lot of time on the visual layout, the interaction design, and how the three leopard panels would work together to show phenotypic variation. The comparison slider was the central interaction I built everything else around.

## What I Learned

Most of what I learned on this project was about UX and visual design decisions. It was the first time I really thought about layout as a design problem rather than just putting things on a page.

A few specific things:

- **Contrast and hierarchy**: The dark background and large typography were a deliberate choice to make the leopard images pop. I had to keep adjusting colors until the text was legible without washing out the imagery.
- **Interaction design**: The drag-to-compare slider was tricky to get right on both mouse and touch. Interactions that feel obvious to you are often confusing to someone seeing the page fresh.
- **Mobile as a different experience**: The desktop interaction (drag sliders, inspect hotspots) does not translate directly to a small screen. I built a separate bottom sheet for mobile hotspot content and added a landscape mode suggestion on load. Making the same content work across screen sizes without it feeling broken was harder than I expected.
- **CSS layout depth**: Writing all the CSS by hand for a layout this layered taught me a lot about stacking contexts, z-index, and how sticky positioning interacts with overflow.

## What It Does

The exhibit has three side-by-side panels showing the same Amur leopard species in different environments and conditions: summer coat, winter coat, and an injured leopard representing the genetic cost of poaching. You can drag sliders between panels to compare them. Clicking a hotspot on the coat or wound brings up more information about that trait.

There is also an artist's statement section that explains the design and biological framing in a Q and A format.

## How to Run

This is a single HTML file with no build step. Open `index.html` in a browser, or serve it locally:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

The live version is deployed on Vercel.

## Sources

- [Earth.org: Amur Leopard](https://earth.org/?endangered-species=amur-leopard)
