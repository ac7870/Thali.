# Thali (static, no API key)

One file, `index.html`. No server, no backend, no environment variables,
nothing to configure. Search 130 foods, log portions against daily targets,
see a seven-day chart. Everything is saved in the browser via localStorage.

There is no photo-reading feature in this version — that required a server
and an API key to talk to Claude. If you want it back later, ask for the
version with the photo panel and its small backend.

## Deploy this in under a minute

**Netlify (drag and drop, easiest):**
1. Go to app.netlify.com/drop
2. Drag `index.html` onto the page
3. It gives you a live URL immediately — done

**Vercel:**
1. Go to vercel.com → Add New → Project → "Deploy without Git" / or drag the file into a new GitHub repo and import it
2. No environment variables needed, no configuration screen to touch — just Deploy

**GitHub Pages:**
1. Create a new repository, upload `index.html`
2. Repository Settings → Pages → Source: deploy from the `main` branch, root folder
3. It publishes at `https://yourusername.github.io/reponame/`

## Editing the food list

Open `index.html` in any text editor, search for `const FOODS = [`, and add a
line following the same pattern:

```js
F("Kothu parotta","South Indian",230,8,26,10,1.8,"1 plate",250),
```

Order: name, category, calories, protein, carbs, fat, fibre — all per 100 g —
then a portion name and its weight in grams.
