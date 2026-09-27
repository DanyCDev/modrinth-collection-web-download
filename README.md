
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
  - Mod loader (Fabric, Forge, Quilt, NeoForge, etc.)
  - Version preference (Prefer stable releases with fallback to Alpha/Beta, or always newest)
  - Mods & Plugins & Data packs, Shaders, Resource packs
- Live progress tracking with logs and stats
- Avoids duplicates
- Error handling for missing versions/files

---


## Share links

The form can be pre-filled from the URL, so a whole modpack setup fits in one short link (e.g. in a server MOTD):

```
https://md.dkg.sk/?c=YV97U1kk&v=1.21.1&l=f
```

| Param | Meaning | Notes |
|-------|---------|-------|
| `c` | Collection ID | |
| `v` | Minecraft version | |
| `l` | Loader | `f` Fabric, `fg` Forge, `q` Quilt, `n` NeoForge, `ll` LiteLoader, `ml` ModLoader, `p` Paper, `b` BungeeCord, `fo` Folia, `pu` Purpur, `s` Spigot, `v` Velocity, `w` Waterfall (full names also work) |
| `s` | `s=0` = newest overall | Omit for "prefer stable" |
| `t` | Included categories: `m` mods/plugins/datapacks, `r` resource packs, `s` shaders | Omit to include all |

The address bar updates as you change the form, and **Copy share link** copies the current link.
