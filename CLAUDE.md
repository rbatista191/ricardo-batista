# ricardobatista.me

Astro static site. Files in `public/` are served as-is. Cloudflare Pages builds and deploys on a push to `main`.

## Jogo de carros (`/jogo`)

A browser car game for Luca (5, dark hair) and Fred (2, blond). All game text is in European Portuguese.

- `public/jogo/index.html` holds all the game code (Three.js r128 from cdnjs, no build step). Edit it directly.
- Do not put other files for the game in `public/` unless the game loads them. Everything there is published.

### Deploy

Deploy after every game change. The user gave standing approval to commit and push game changes to `main`.

```bash
SITE=/Users/rbatista19/Developer/ricardobatista.me/ricardo-batista
(cd $SITE && npm run build)
git -C $SITE add public/jogo/index.html
git -C $SITE commit -m "<STE100 message>"
git -C $SITE push origin main
```

Poll `curl -s https://ricardobatista.me/jogo/ | grep <new string>` until the change is live.

### Test

- Extract the script and run `node --check` on it.
- Use Playwright headless (Chromium with swiftshader) to drive the car and check the feature works.
- Check the phone layout too: touch buttons show on touch devices.

### Notes

- The game uses Disney/Pixar, Lucasfilm and DC characters (McQueen, Mater, Toy Story items, Grogu, Batmobile). The user knows about the IP risk of a public site and chose to deploy.
