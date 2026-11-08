# MashWave

A monochrome, space-inspired, local-first music workspace for Geometry Dash players. This is an original standalone HTML/CSS/JavaScript project.

## Run it

1. Extract the folder.
2. Open `index.html` in current Microsoft Edge or Google Chrome.
3. Import audio files from **Music library**. MashWave uses IndexedDB to store audio in the current browser profile.

If your browser restricts storage or audio metadata when opening files directly, run a tiny local server from this folder:

- Python installed: `python -m http.server 8000`
- Then open `http://localhost:8000`.

No Node.js, account, server, or build step is required.

## Features

- Original black-and-white, orbital space aesthetic with responsive layout.
- Import audio files, drag and drop, search, sort, favorite, rename, delete, and preview tracks.
- Persistent audio storage using IndexedDB (subject to browser storage quotas).
- Playback controls, seek, volume, and next/previous track.
- Map local tracks to Geometry Dash song IDs; enable/disable, edit, filter, and delete mappings.
- Export mappings as JSON or CSV; import JSON mappings; export library metadata.
- Local-first: your audio files are not uploaded.

## Important limitation

MashWave's website stores and exports song mapping data; it **does not change music inside Geometry Dash by itself**. That requires a compatible Geode mod or another game-side integration that reads the exported mapping format and handles audio replacement. The site does not pretend that such a connection already exists.

## Storage notes

Audio blobs stay in IndexedDB in this browser profile. Clearing browser site data may delete them. The library metadata export does not contain the actual audio files, so keep your original audio files backed up separately.
