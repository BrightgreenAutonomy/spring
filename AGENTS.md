## Cursor Cloud specific instructions

This is a single-file static website (`index.html`) with no dependencies, no build step, and no package manager.

### Running the dev server

```
python3 -m http.server 8000 --directory /workspace
```

The site is then available at `http://localhost:8000/`.

### Testing

There are no automated tests, linters, or build commands. Validation is done by:
- Opening the site in a browser and verifying it renders correctly
- Checking that navigation links smooth-scroll to the correct sections
- The CI workflow (`.github/workflows/static.yml`) only deploys to GitHub Pages; there is no test/lint CI step

### Deployment

Production deploys happen automatically via GitHub Pages on push to `main`.
