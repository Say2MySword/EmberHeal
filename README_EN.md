# EmberHeal

[中文](README.md) | English

**HealBot-style healing frame for Emberveil** · for the Emberveil client (WoW 1.12.1 emulation / Lua 5.1 API) · current version 1.0.13

## Features

- **Raid / party health grid**: draggable with position memory, white name and health text on each bar
- **Click casting**: bind **left / right click** (with optional Shift / Ctrl / Alt) to action bar spells on the "Click Cast" page, then click a unit frame to cast (casting goes through action slots; a binding auto-rotates to the next occupied slot)
- **Dispel indicators**: debuff icons on each bar, colored by type — magic / disease / poison / curse each have their own glyph
- **Buff watch**: remaining time and expiry alerts for tracked buffs; the watch list is configurable on the "Watch" page
- **Range & aggro**: bars dim when the target is out of casting range; border highlights on aggro
- **Hover info**: dead / offline / out of range / aggro / debuff type at a glance
- **Options panel**: three pages (Display / Click Cast / Watch), every toggle has a hover tooltip
- **Bilingual UI**: English and Chinese, switched automatically by client locale
- **Minimap button**: left click toggles the grid; right click / Shift+left opens the options panel; drag to orbit the minimap
- Zero third-party libraries, pure Lua 5.1

## Install

1. Download `EmberHeal-1.0.13.zip` from the Releases page and extract it
2. Put the whole `EmberHeal` folder into `...\Emberveil\live\Azeroth\Interface\AddOns\`
3. Re-log (or `/reload`) and you are set

## Usage

- **Toggle the grid**: click the minimap button, or adjust display settings in the options panel
- **Bind spells**: options panel → "Click Cast" page → click a row, then click a spell on your action bar; bound rows can be cleared with one click
- **Three option pages**:
  - Display: scale, health percentage, font size and other display toggles
  - Click Cast: mouse-button-to-spell binding management
  - Watch: buff / debuff watch lists

## Known limitations

- The client engine does not deliver **middle mouse button / side button** events to Lua UI (engine limitation, not workable from the addon side), so click casting currently supports left / right buttons with modifier keys only.

## License

MIT License
