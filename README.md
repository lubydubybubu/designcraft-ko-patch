# designcraft-ko-patch

Korean (한국어) interface patch for **[DesignCraft](https://github.com/storytold/designcraft)** (InDesign-class page layout), upstream tag `v0.7.1`.
This repository contains **only the patch**, not DesignCraft's source code. See `BASE.txt` for the exact upstream commit.

## Apply
```bash
git clone --branch v0.7.1 https://github.com/storytold/designcraft.git && cd designcraft
git apply ../designcraft-ko-patch/patches/designcraft-v0.7.1-ko.patch
```
Then build as upstream documents. Windows build without MSVC: [artcraft-ko-toolkit](https://github.com/lubydubybubu/artcraft-ko-toolkit).

## What it changes
Korean catalog ported from storytold/designcraft PR #395 (con3code), 92 rows revised to Korean InDesign terms, 16 added; Hangul UI font (embedded Noto CJK when built with craft-fonts 8dcdacd+, else Malgun Gothic); first launch follows the Windows locale.
Changed files: `CHANGED-FILES.txt`.

## Verified
11 Korean tests RED→GREEN, ui-egui lib 190 passed; Windows headless render: Korean menus/panels, no tofu.

## Known limits
Panel/layout strings outside the catalog stay English; Windows locale probe uses reg.exe.

Translations are AI-assisted (Claude Opus 5.5) and not reviewed by a professional translator.
Licence: MIT OR Apache-2.0, same as DesignCraft; upstream contributions credited above.
