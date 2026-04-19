# hommyeg (WebGL for GitHub Pages)

## Fix for 404 on `Build/*.loader.js`

This folder used a **Unity project `.gitignore`** that contained `/Build/`, so Git **never tracked** the WebGL `Build/` folder — GitHub had no loader/wasm/data files. That rule was removed here.

## Required files after a Unity WebGL build

Your `Build/` folder must include **all** outputs, for example:

- `hommyeg.loader.js`
- `hommyeg.framework.js`
- `hommyeg.data`
- `hommyeg.wasm`

If `.data` / `.wasm` are missing locally, **rebuild in Unity** (File → Build Settings → WebGL → Build) and copy the **entire** build output into this repo (keep the same structure as Unity produced).

Then commit and push **including** the `Build/` directory.

## GitHub Pages

`.nojekyll` is present so Jekyll does not skip needed files.
