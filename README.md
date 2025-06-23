# Reproduction for Biome.js Vite Config Comment Duplication Bug

This repository demonstrates an issue where Biome.js duplicates a top-line comment in `vite.config.js` when sorting imports with `:BLANK_LINE:`.

## Issue Description
When running `biome check --write` on a `vite.config.js` file:
1. The import sorting duplicates the first-line comment (`// some comment`).

## Steps to Reproduce
1. This repository already contains:
   - A `vite.config.js` file with unsorted imports and a top-line comment `// some comment`
   - Biome configuration with `:BLANK_LINE:` sorting rule
2. Run the command:
   ```
   biome check --write ./vite.config.js
