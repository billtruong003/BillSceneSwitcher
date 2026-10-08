# Changelog

## [2.0.0] - 2026-10-08

First release as a standalone UPM package (previously shipped inside BillGameCore). Successor of
`com.billtruong003.sceneswitcher` 1.x.

- Namespace `BillGameCore.BillSceneSwitcher` → `BillSceneSwitcher`; assembly renamed to
  `BillSceneSwitcher`.
- Menu moved from `BillGameCore/Scene Switcher…` to `Tools/Bill/Scene Switcher…`; toolbar element id
  is now `Bill/Scene Switcher` (re-enable it once from the toolbar's context menu if it disappears).
- Default project folders `Assets`, excluded folders `Assets/Samples;Assets/Plugins` (were specific to
  one game).
- Default data asset path is now `Assets/Settings/Editor/BillSceneSwitcherData.asset` (an existing
  asset anywhere in the project is still found).
- Requires Unity 6000.3+ (`MainToolbar` API).
