# Lantern

An HTML5 canvas game, deployed on Cloudflare Pages and embedded (iframe) into another website.

Survival horror, isometric low-poly. Your cursor is the only light. A crowd of frightened villagers
follows it, and the dark follows them. The village burned; the road to the city runs through the wood,
nine safe houses long. The last lantern-bearer did not come back. The game narrates your mistakes, by
name, and it has walked this road before.

- `public/index.html` — the entire game (no build step, no dependencies, no asset files)
- `wrangler.jsonc` — Cloudflare Pages config (`assets.directory: ./public`)

## How to play

- Move the mouse. Villagers walk toward the light and huddle in it.
- Anyone left in the dark too long panics and runs. Panicked people walk into ditches.
- The light draws the dark too. Things that reach the bright core of the lantern burn.
  Anything that reaches a villager outside the core takes them. There is no getting them back.
- The oil burns down over the night. Pass the light over flasks on the road to refill it.
- Gusts gutter the flame for a moment. The dark rushes when it does.
- Things in the dark call villagers by name. The one called will drift toward the voice unless the light holds them.
- The road is blocked along the way. A fallen tree needs three villagers working in the light. A broken
  bridge needs two. A gate lock only turns while the lantern sits on it. The dark gathers while you stand.
- Nine houses to the city. Reach the gate and the road goes on.
- Click to drop a salt line (if you bought salt). `M` mutes, `P` pauses.
- Between nights, the village pays per head delivered. Spend it on a brighter lantern, a bell,
  courage, torchbearers, dogs and salt.

## Run locally

    python3 -m http.server 8000 -d public

## Deploy

    npx wrangler pages deploy

## Embed

    <iframe src="https://<your-pages-domain>/" width="540" height="960" style="border:0" allow="autoplay"></iframe>

The game letterboxes a 540x960 playfield to any iframe size.
