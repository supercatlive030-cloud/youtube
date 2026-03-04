# The Game Website (Static scaffold)

This is a minimal static website to host browser games. It includes a small launcher page that reads `games/games.json` and displays the listed games. Each game should be placed inside `games/<your-game>/` with an `index.html` entry point.

How to add a game
- Create a folder `games/your-game-name/`.
- Add an `index.html` inside that folder that loads your game assets and scripts.
- Add an entry to `games/games.json` with the `path` pointing to the game's `index.html` (relative path starting at the site root).

Example `games/games.json` entry:

```
{
  "id": "mygame",
  "title": "My Game",
  "path": "games/mygame/index.html",
  "description": "Short description"
}
```

Serve locally
- Python 3:

```bash
python -m http.server 8000
```

- Node (if you have `http-server`):

```bash
npm install -g http-server
http-server -c-1
```

Then open `http://localhost:8000` in your browser.
