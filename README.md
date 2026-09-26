# Elemental Sandbox

A falling-sand style cellular automaton sandbox that runs entirely in the browser. No dependencies, no build step — just open `index.html`.




## Elements

| Element | Behavior |
|---|---|
|  **Sand** | Falls, piles up, sinks through water |
|  **Water** | Flows and spreads horizontally, shimmers |
|  **Wood** | Solid platform, flammable |
|  **Fire** | Rises, ignites wood & plants, turns water into steam |
|  **Plant** | Slowly grows into adjacent water, flammable |
|  **Microbe** | Swims in water, eats plants, reproduces by splitting, dies of old age |
|  **Steam** | Rises from fire + water, condenses back into water |
|  **Wall** | Indestructible solid |

## Microbes

Microbes are simple autonomous agents with an energy system:

- **Swim** in water using wander movement (random direction changes)
- **Eat plants** to gain energy
- **Lose energy** on land — they can only crawl ashore briefly
- **Reproduce** by splitting when energy is high
- **Die** when energy runs out, lifespan ends, or they touch fire

## Controls

- **Draw** — click / drag with mouse or touch
- **Brush size** — slider in the control bar
- **Pause / Play** — freeze the simulation
- **Clear** — wipe the world
- **Grid** — toggle a faint grid overlay

## Running locally

Just open `index.html` in any modern browser. Or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
