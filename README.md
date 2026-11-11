
# Modrinth Collection Downloader

A fully client-side web app that allows you to download all mods from a **Modrinth collection** and package them into a single `.zip` file entirely from your browser. [Try it for yourself - https://md.dkg.sk](https://md.dkg.sk)

---

<img width="1242" height="1729" alt="obrázok" src="https://github.com/user-attachments/assets/2b7634a5-b3a9-4980-992d-81204e3dcd36" />


---

## Features

- Accepts Modrinth collection ID or URL
- Downloads all mods in a collection and puts them into a ZIP file
- Automatically downloads all required dependencies
- Filters by:
  - Minecraft version
  - Mod loader (Fabric, Forge, Quilt, NeoForge, etc.) with optional **fallback mod loader** (useful when combining loaders, e.g. NeoForge + Fabric via connector)
  - Version preference (Prefer stable releases with fallback to Alpha/Beta, or always newest)
  - Mods & Plugins & Data packs, Shaders, Resource packs
- Shareable links: pre-fill the form with URL query parameters and copy with one click
- Live progress tracking with logs and stats
- Avoids duplicates
- Error handling for missing versions/files

---

## Share links

The form can be pre-filled from URL query parameters, so a full modpack setup fits in one short link (e.g. in a server MOTD or Discord):

```
https://md.dkg.sk/?c=YV97U1kk&v=1.21.1&l=n&fl=f
```

| Param | Meaning | Notes |
|-------|---------|-------|
| `c` | Collection ID | Accepts ID or collection URL |
| `v` | Minecraft version | e.g. `1.21.1` |
| `l` | Primary mod loader | `f` Fabric, `fg` Forge, `q` Quilt, `n` NeoForge, `ll` LiteLoader, `ml` ModLoader, `p` Paper, `b` BungeeCord, `fo` Folia, `pu` Purpur, `s` Spigot, `v` Velocity, `w` Waterfall (full names also work) |
| `fl` | Fallback mod loader | Same loader codes as `l` (omitted if None) |
| `s` | `s=0` = newest overall | Omit for "prefer stable" (default) |
| `t` | Included categories | Combination of `m` (mods/plugins/datapacks), `r` (resource packs), `s` (shaders). Omit to include all |

Expand **Advanced options** and click **Copy share link** to copy the share link to clipboard. The address bar stays clean on `/` while you browse and configure options.

---

