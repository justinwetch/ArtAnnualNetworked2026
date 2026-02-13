# Token Dynamic

A network visualization where each minter in a collection is represented as a floating ART icon, labeled with their name, drifting through a dark canvas. When nodes drift close enough to each other, lines appear between them — closer means brighter, farther means the line fades away. The result is an organic, constantly shifting constellation of the minter community.

## How It Works

The canvas spawns one ART image per minter. Each node floats on its own unique sinusoidal path, so no two move alike. Proximity between nodes drives the connecting lines — forming and dissolving as the network breathes.

## Making It Dynamic

Right now the minter count and names are fixed. The goal is to make this fully dynamic: the system would need a way to know **how many** minters exist and **what each one is called**, then spawn exactly that many ART nodes with the correct name beneath each.

This means the visualization needs to:

- **Read from a source of truth** for the current list of minters — who they are, how many there are
- **Spawn one ART node per minter**, each carrying that minter's name as its label
- **Adapt its layout** to the count — spacing, icon size, and connection distances should feel right whether there are 5 nodes or 50
