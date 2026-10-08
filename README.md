# Bill Scene Switcher

A scene switcher on Unity 6.3's **main toolbar**. One click shows every scene in the project; type to
search, press Enter to open. It also runs **Play from bootstrap**: enter Play Mode through your boot
scene and come back to the scene you were editing afterwards.

## Features

- **Two tabs:** *In build* (bootstrap, pinned, Build Settings, recent) and *Out of build* (every other
  scene, grouped by folder, filtered by chips such as project scenes vs. bought assets).
- **Search** across all scenes; ↑/↓ to move, Enter to open, Shift+Enter to open additively.
- **Pin** scenes (drag to reorder), including scenes that are not in the build.
- **Build Settings from the list:** add, remove, enable/disable a scene, with undo.
- **Set as bootstrap** puts a scene at build index 0.
- **Play from bootstrap:** saves your open scene setup, opens the bootstrap scene, enters Play Mode,
  and restores the setup when you stop.
- Additive open/close buttons on each row; recent scenes; scene path display.

## Install

Package Manager → **Add package from git URL…**

```text
https://github.com/billtruong003/BillSceneSwitcher.git#v2.0.0
```

Editor-only. Requires **Unity 6000.3+** (it uses the `MainToolbar` API added in 6.3).

## Use

- Click the scene button on the main toolbar, or **Tools ▸ Bill ▸ Scene Switcher** (Ctrl+Shift+S).
  If the button is missing, right-click the toolbar and enable **Bill/Scene Switcher**.
- Right-click a scene for: open, open additively, pin, enable/disable in build, remove from build,
  set as bootstrap, show in Project, copy path.
- **▶ Play from Bootstrap** sits at the bottom of the panel.

## Settings

**Edit ▸ Preferences ▸ Bill Scene Switcher** (toolbar and additive toggles also under
**Tools ▸ Bill ▸ Scene Switcher**):

| Setting | Default | |
|---|---|---|
| Project folders | `Assets` | `;`-separated; scenes here count as "project" scenes, the rest as bought assets. Set it to your own folders (e.g. `Assets/_Game`) so the filter chips mean something |
| Excluded folders | `Assets/Samples;Assets/Plugins` | `;`-separated; hidden from the list |
| Recent scenes | 3 | 0–10 |
| Show scene path | on | |
| Show additive button | on | |
| Ask to save when switching | on | |
| Show toolbar button | on | |

These are per-user (`EditorPrefs`).

## Where the data lives

Pins and the bootstrap choice are stored in a `BillSceneSwitcherData` asset, created on first use at
`Assets/Settings/Editor/BillSceneSwitcherData.asset` unless one already exists elsewhere. Commit it to
share pins with the team.

## Notes

- The interface text is Vietnamese in this version. An English translation is planned.
- Ctrl+Shift+S is also Unity's *Save As*. Rebind either in **Edit ▸ Shortcuts**.
- Replaces the older [SceneSwitcherToolUnity](https://github.com/billtruong003/SceneSwitcherToolUnity)
  (`com.billtruong003.sceneswitcher` 1.x).

## License

MIT, see [LICENSE.md](LICENSE.md).
