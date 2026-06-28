# EldenRimTogether - Wabbajack Modpack

## Project Overview

**Modpack Name:** EldenRimTogether
**Current Version:** 3.4.2
**Purpose:** A comprehensive Skyrim Special Edition modpack combining Skyrim Together Reborn multiplayer functionality with Elden Ring-inspired combat mechanics
**Distribution:** Wabbajack installer
**Mod Organizer 2:** v2.5.2 ML1.5 (Windows)
**RootBuilder:** v5.0.5.0

## Project Structure

```
modpack updating/
├── CLAUDE.md                                     # This file - project documentation
├── AGENTS.md                                     # Pointer to CLAUDE.md (single source of truth)
├── README.md                                     # Public repo readme (footer links to Changelog)
├── Changelog                                     # Player-facing changelog (committed + pushed)
├── EldenRimTogether-Wabbajack-Changelog-X.X.X.md # Internal versioned changelogs (latest = highest version)
├── changelog_scanner.py                          # Automated changelog generation tool
├── test_changelog_scanner.py                     # Scanner test suite (run after scanner changes)
├── mod_versions_before.txt                       # Version baseline (frozen at last confirmed scan)
├── mod_versions_after.txt                        # Version snapshot taken at scan time
├── modlist_before.txt                            # Enable-state baseline (frozen at last confirmed scan)
├── Start Nexus Runner.bat                        # Launches self-hosted runner for Nexus uploads
├── elden-together-resources/                     # Clone of the Nexus upload workflow repo
├── startup dashboard backup/                     # Backup of StartupDashboard rules.json + presets
└── build_logs/                                   # Tool output logs
```

### Key Files
- **Changelog (.md)**: Master document tracking all mod changes, versions, and updates
- **Mod Organizer 2 Profile**: Contains load order, mod configurations, and enabled/disabled states
- **Wabbajack Manifest**: Build instructions for the automated installer

## Modpack Maintenance Guidelines

### Changelog Format
All changes must be documented in the changelog file using this format:

```
MM/DD/YYYY HH:MM UTC :: Launch - [Status]
// Comment describing the update
```

#### Changelog Legend
```
+ = Added Mod
- = Removed Mod
E = Enabled Mod
D = Disabled Mod
M = Modified Mod (Include summary of changes)
// = Comment (C-style comments)
```

#### Example Entry
```
11/10/2025 04:15 UTC :: Launch - Success
// Version 3.2.9 - Multiple mod updates and additions

# 01.2 MODDER RESOURCES - UTILITIES - CORE FIXES
+E Dynamic Interface Patcher - DIP // Added
M Navigator - Navmesh Fixes // Updated from 1.6.3 to 1.8.0
M Papyrus Tweaks NG // Updated from 4.1 to 4.1.1
```

### Version Number Convention
- **Major.Minor.Patch** (e.g., 3.2.9)
- Increment patch for mod updates
- Increment minor for significant feature additions
- Increment major for complete overhauls

#### Modlist Update Checker Behavior (In-Game Notifications)
This modpack uses the **Modlist Update Checker** SKSE plugin to notify players of updates in-game. Versioning directly controls what notification players see:
- **Patch bump** (e.g., 3.3.0 → 3.3.1) = "This update is **save-safe**" notification 🟢
- **Minor bump** (e.g., 3.3.0 → 3.4.0) = "This update **requires a new save**" notification 🔴
- **Major bump** (e.g., 3.3.0 → 4.0.0) = "This update **requires a new save**" notification 🔴

> ⚠️ Always increment versions correctly! Players rely on these notifications to know if they need to start a new save.

### Best Practices for Mod Management

1. **Before Adding/Updating Mods:**
   - Check Skyrim Together Reborn compatibility
   - Verify SKSE version requirements
   - Test in single-player before multiplayer
   - Document version numbers in changelog

2. **Category Organization:**
   - Place mods in appropriate numbered categories (see categories below)
   - Maintain load order within categories
   - Keep category 99 (UNSORTED) for temporary/testing mods

3. **When Updating Mods:**
   - Note old version → new version in changelog
   - Check for new dependencies or patches
   - Review mod page for breaking changes
   - Test after updating before pushing changes

4. **Removing Mods:**
   - Use `-D` (removed and disabled) in changelog
   - Keep entry in changelog for historical reference
   - Document reason in comment if significant

## Skyrim Together Reborn Integration

### Key Category: 16.4 SKYRIM TOGETHER REBORN
This category contains multiplayer-specific mods:
- Skyrim Together Reborn Features Integration
- Compatibility patches for STR

### Multiplayer Compatibility Considerations

**Compatible Systems:**
- Animation frameworks (OAR, Nemesis, Pandora)
- UI enhancements (SkyUI, TrueHUD)
- Visual overhauls (textures, meshes, lighting)
- Shared gameplay mechanics

**Requires Special Attention:**
- Quest mods (may desync)
- Follower mods (can cause issues)
- Save-dependent scripts
- NPC AI modifications
- Dynamic world changes

**Testing Protocol:**
1. Test mod in single-player
2. Test with 2 players in controlled environment
3. Test quest progression sync
4. Test combat mechanics synchronization
5. Document any desyncs or issues

## Mod Category System

### Core Framework (01.x)
- **01.1** - Early Loaders (Core requirements loaded first)
- **01.2** - Modder Resources, Utilities, Core Fixes (SKSE, frameworks, fixes)

### User Interface (02.x)
- **02.1** - Console (Console improvements and extensions)
- **02.2** - HUD (Health, stamina, compass, detection meter)
- **02.3** - UI (Menus, inventory, interaction)
- **02.4** - Camera (Third person, smoothcam)
- **02.5** - Maps (World map, local map)
- **02.6** - Controls (Input, movement)

### Audio (03.x)
- **03.1** - Audio & Sound
- **03.2** - Music

### Visuals (04.x - 05.x)
- **04.1** - Base Meshes & Textures
- **04.2** - Architecture
- **04.3** - Landscape
- **04.4** - Caves & Mines
- **04.5** - Water, Snow, Ice
- **04.6** - Weathers & Sky
- **04.7** - Lighting
- **05.1** - Clutter, Furniture, Decorations
- **05.2** - Items, Misc, Ingredients, Containers
- **05.3** - Plants, Food, Alchemy

### Gameplay (09.x - 13.x)
- **09.5** - Gameplay - Survival & Immersion
- **12.1** - Body, Skin, Face
- **13.1** - Armors (Replacers)
- **13.2** - Weapons (New additions)
- **13.4** - Clothing & Items
- **13.5** - Jewelry

### Combat System (14.x)
- **14.1** - Combat (Frameworks: BFCO, Precision, Elden Parry)
- **14.2** - Combat Movesets (Weapon animations: Vanargand, Leviathan, Goetia, Elden Rim)
- **14.3** - Movement Animations (Sprint, walk, run by gender)
- **14.4** - Idles & Other Animations (Sitting, leaning, gestures)

### Integration & Patches (15.x)
- **15.1** - SPID Distribution (Item/spell distribution)
- **15.2** - Miscellaneous Patches & Bug Fixes
- **15.3** - Performance
- **15.4** - Late Loaders (Load last, UI overhauls)
- **15.5** - MCM Helper & Settings Loaders
- **15.6** - DynDOLOD

### Multiplayer (16.x)
- **16.4** - Skyrim Together Reborn

### Build Outputs (17.x - 18.x)
- **17.2** - Synthesis Output
- **17.3** - Bodyslide Output
- **17.4** - Pandora Output
- **17.5** - Wrye Bash Output
- **17.9** - Mod Settings
- **18.0** - LODGen Output
- **18.1** - TexGen Output
- **18.2** - DynDOLOD Output
- **18.3** - Mod Patches

### Testing (99)
- **99** - UNSORTED (Recent additions, testing)

## Build Process

### Required Tools
1. **Mod Organizer 2** v2.5.2 ML1.5 - Mod management
2. **RootBuilder** v5.0.5.0 - Root folder file management
3. **Pandora Behaviour Engine Plus** - Animation/behavior engine (Nemesis-compatible; Nemesis Unlimited remains installed but Pandora generates the 17.4 output)
4. **Synthesis** - Automated patching
5. **DynDOLOD** - LOD generation
6. **TexGen** - Terrain LOD textures
7. **Wrye Bash** - Bashed patch creation
8. **BodySlide** - Body mesh generation

### Build Order
1. Install all mods through Mod Organizer 2
2. Run BodySlide to build meshes → Output to **17.3**
3. Run Pandora to generate animations/behaviors → Output to **17.4**
4. Run Synthesis for automated patches → Output to **17.2**
5. Run Wrye Bash for leveled lists → Output to **17.5**
6. Run TexGen for terrain textures → Output to **18.1**
7. Run LODGen for object LODs → Output to **18.0**
8. Run DynDOLOD for dynamic LODs → Output to **18.2**
9. Apply final patches to **18.3**
10. Configure mod settings in **17.9**

### Post-Build Testing
- Launch game through Mod Organizer 2
- Verify SKSE loads correctly
- Check MCM menus load properly
- Test new game character creation
- Test save/load functionality
- Test with Skyrim Together Reborn client

## Instructions for Claude Code

When assisting with this modpack:

1. **Always Reference the Changelog First**
   - **IMPORTANT:** Always use the LATEST changelog file (check version numbers in filenames)
   - Current latest: `EldenRimTogether-Wabbajack-Changelog-3.4.2.md`
   - Maintain consistency with existing formatting
   - Note version numbers for updated mods

2. **Maintain Category Organization**
   - Place new mods in appropriate numbered categories
   - Follow the load order logic (early loaders first, patches last)
   - Keep outputs in 17.x and 18.x categories

3. **Document All Changes**
   - Use the changelog legend (+, -, E, D, M, //)
   - Include timestamps in UTC
   - Add comments explaining significant changes
   - Note "Launch - Success" or "Launch - Unknown" status

4. **Version Tracking**
   - Always document "Updated from X.X to Y.Y"
   - Increment modpack version appropriately
   - Update filename if creating new changelog version

5. **Multiplayer Considerations**
   - Flag any mods that might affect Skyrim Together Reborn
   - Suggest testing protocol for multiplayer compatibility
   - Check for known STR incompatibilities

6. **Conflict Resolution**
   - Check for mod conflicts before suggesting additions
   - Verify patch requirements

7. **Build Process Awareness**
   - Remind about rebuild requirements (Pandora, Synthesis, etc.)
   - Note if changes require LOD regeneration
   - Suggest testing steps based on change type

## Automated Changelog Generation Workflow

**Tool:** Python scanner located at `C:\Users\DJLegnds\Downloads\Mods\modpack updating\changelog_scanner.py`
**Tests:** `python test_changelog_scanner.py` — run after any changes to the scanner

### File Locations
- **Mod Installation:** `D:\Modlists\Elden\mods`
- **Profile/Load Order (live):** `D:\Modlists\Elden\profiles\EldenRim With Friends\modlist.txt`
- **Meta.ini Files:** Each mod folder contains a `meta.ini` with version info on line 4
- **Version Snapshot Files:** `C:\Users\DJLegnds\Downloads\Mods\modpack updating\mod_versions_before.txt` and `mod_versions_after.txt` (in workspace)
- **Modlist Baseline (workspace):** `C:\Users\DJLegnds\Downloads\Mods\modpack updating\modlist_before.txt` — a frozen copy of the live profile modlist captured at the last confirmed scan. **Not** the current modlist (the live profile file is always source of truth). The scanner diffs this against the live profile modlist to detect enable/disable flips that don't show up in version snapshots.
- **Modlist Update Checker INI:** `D:\Modlists\Elden\mods\Modlist Update Checker\skse\plugins\ModlistUpdateChecker.ini`
- **MO2 Version Separator:** `D:\Modlists\Elden\mods\-_________________________________ ELDENRIM TOGETHER - X.X.X ________________________________________separator`

### Workflow Steps

The `mod_versions_before.txt` AND `modlist_before.txt` files persist in the workspace between sessions as the baseline pair. Neither is the current state — the current state is read live from `D:\Modlists\Elden\mods\*\meta.ini` and the profile `modlist.txt`. The workspace files are frozen snapshots from the last confirmed scan, only used as the diff anchor.
**TRIGGER:** When user says "scan now", "update complete", or similar.

**Step 1: Check Existing Baselines**
- Verify `mod_versions_before.txt` AND `modlist_before.txt` both exist in the workspace
- If either is missing (first run or deleted), take a fresh baseline (snapshot meta.ini versions into `mod_versions_before.txt` AND copy the live profile modlist into the workspace as `modlist_before.txt`) FIRST, then have the user make their changes before scanning

**Step 2: Scan for Changes**
Take the version AFTER snapshot and run the scanner. The scanner reads the live profile `modlist.txt` directly for current state — no need to copy it anywhere.
```bash
cd /d/Modlists/Elden/mods && \
find . -maxdepth 2 -name "meta.ini" -exec grep -H "^version=" {} \; 2>/dev/null | \
grep -v "separator" | grep -v "version=$" | \
sed 's|./||; s|/meta.ini:version=| :: |' | sort > "/c/Users/DJLegnds/Downloads/Mods/modpack updating/mod_versions_after.txt"
```
```bash
cd "C:\Users\DJLegnds\Downloads\Mods\modpack updating" && python changelog_scanner.py
```

The scanner now reports five change types:
- `M` updates (version changed in `meta.ini`)
- `+E` additions (new mod folder on disk, enabled in live profile modlist)
- `-D` removals (mod folder gone from disk)
- `E` re-enables (was `-` in `modlist_before.txt`, now `+` in live profile modlist)
- `D` disables (was `+` in `modlist_before.txt`, now `-` in live profile modlist)

> # ⚠️ STOP — MANDATORY REPORT-BACK AFTER EVERY SCAN ⚠️
>
> **After running the scanner, ALWAYS show the user the FULL scanner output — changelog entries, VERIFICATION WARNINGS, and summary — and WAIT for their explicit verification before doing ANYTHING else.** Do not write changelog entries, do not sync versions, do not overwrite baselines until the user has confirmed the results are correct.
>
> The scanner prints a `=== VERIFICATION WARNINGS ===` section listing its known blind spots for that scan — these REQUIRE human judgment:
> - **UNVERSIONED** — mods with no `version=` in meta.ini (build outputs, manual patches); the version scan can never see changes to these
> - **POSSIBLE FALSE -D** — reported removed but still in the live modlist (version was probably blanked, not uninstalled)
> - **POSSIBLE FALSE +E** — reported added but already existed in the baseline modlist (version was newly assigned, not a new install)
> - **UPDATED/ADDED WHILE DISABLED** — real changes that are NOT in the entries above and are lost forever once baselines are overwritten
> - **NOT IN PROFILE MODLIST** — mod folder on disk with no profile entry
> - **Possible renames** — a `-D`/`+E` pair with similar names is probably ONE renamed mod; ask the user and log it as `M` instead
>
> Relay these warnings to the user verbatim — never silently resolve them yourself.

**Step 3: Add Results to Changelog (BOTH files)**
- Scanner outputs changes organized by category
- Format: `M ModName // Updated from X.X.X to Y.Y.Y`
- Format: `+E ModName // Added version X.X.X`
- **Update both files in this order:**
  1. **First — local versioned `.md` file** in workspace (e.g. `EldenRimTogether-Wabbajack-Changelog-3.4.0.md`). This is the source of truth and stays untracked unless the user says otherwise.
  2. **Then — `Changelog` (repo root)** — mirror the same entries into the matching `# Version X.Y.Z` section. This is the file the README footer links to, so players see it.
  3. **Commit + push `Changelog` to remote.** The local `.md` doesn't need pushing unless explicitly tracked.
- If bumping to a new version that doesn't yet have a section in `Changelog`, add a new `# Version X.Y.Z` heading at the top of `Changelog` (right under the master header, above the previous newest version) so newest stays first.
- If adding a new dated scan block to an existing version, insert it ABOVE the previous newest dated block within that version's section (and add `---` between blocks).
- **Exception — unshipped hotfixes:** If the prior dated block under the current version has NOT been built into the Wabbajack list and pushed to players yet, MERGE the new scan into that existing dated block instead of creating a fresh one. Players haven't seen the old block — it's not a separate fix, it's the same hotfix growing. Combine the `// comment` headers and fold the new `M`/`+E`/`-D`/`E`/`D` lines into the existing category sections (alphabetize within each category if helpful). Only spawn a new dated block once the prior one has actually shipped. **When in doubt, ask the user** whether the previous block has been pushed to Wabbajack.

**Step 4: Sync Modpack Version Targets**
- Do this only after the user confirms the changelog entry and the intended modpack version.
- Keep these three version targets synchronized:
  - Latest changelog filename/header/version entry
  - `Version = X.X.X` in `D:\Modlists\Elden\mods\Modlist Update Checker\skse\plugins\ModlistUpdateChecker.ini`
  - MO2 top separator folder and matching `modlist.txt` line: `ELDENRIM TOGETHER - X.X.X`
- Version bump meaning matters:
  - Patch/hotfix bump = save-safe notification
  - Minor/major bump = new-save-required notification
- Editing the INI, renaming the separator folder, or updating `D:\Modlists\Elden\profiles\EldenRim With Friends\modlist.txt` writes outside the workspace and requires user permission.

**Step 5: Save New Baseline**
- **5a:** Ask the user to verify and confirm the changelog and version-sync changes before overwriting the baselines
- **5b:** Once confirmed, overwrite BOTH baselines — the version snapshot AND the modlist baseline — so the next scan starts from the post-confirmation state:
```bash
cp "/c/Users/DJLegnds/Downloads/Mods/modpack updating/mod_versions_after.txt" "/c/Users/DJLegnds/Downloads/Mods/modpack updating/mod_versions_before.txt"
cp "/d/Modlists/Elden/profiles/EldenRim With Friends/modlist.txt" "/c/Users/DJLegnds/Downloads/Mods/modpack updating/modlist_before.txt"
```

### How the Scanner Works

The Python scanner (`changelog_scanner.py`):
1. **Loads version snapshots** from `mod_versions_before.txt` and `mod_versions_after.txt` in the workspace directory
2. **Parses two modlists** with `parse_modlist`:
   - Live profile modlist at `D:\Modlists\Elden\profiles\EldenRim With Friends\modlist.txt` — current category map and current enable state
   - Workspace baseline `modlist_before.txt` — last confirmed enable state, used only as the diff anchor
   - Reads in REVERSE order (critical!): modlist.txt has bottom = loaded first, top = loaded last; category separators sit BELOW their mods in the file, so reading bottom-to-top assigns categories correctly. Mod lines are prefixed `+` (enabled) or `-` (disabled).
3. **Detects version changes** (`detect_changes`):
   - `M` Updates: version changed
   - `+E` Additions: mod exists in AFTER but not BEFORE (only reported when currently enabled)
   - `-D` Removals: mod exists in BEFORE but not AFTER
4. **Detects state changes** (`detect_state_changes`):
   - `E` Re-enables: was disabled in `modlist_before.txt`, now enabled in live profile modlist
   - `D` Disables: was enabled in `modlist_before.txt`, now disabled in live profile modlist
   - Only mods present in both modlists are considered — pure adds/removes are handled by the version-scan path so they don't double-count
5. **Can sync modpack version targets after approval**:
   - Updates Modlist Update Checker `Version = X.X.X`
   - Renames the MO2 top separator folder
   - Updates the matching separator line in `modlist.txt`
6. **Outputs organized results** grouped by category

### Usage Notes
- **Baseline pair persists in workspace** — `mod_versions_before.txt` (versions) AND `modlist_before.txt` (enable state + load order). Both are overwritten together in Step 5 only after user confirmation. The live profile `modlist.txt` is always the source of truth; the workspace copy is just a frozen anchor for diffing.
- **User can update any number of categories** at once
- **Scanner detects updates, additions, removals, enables, AND disables** across all 600+ mods. Pure load-order moves (no `+`/`-` flip) are ignored on purpose.
- **Categories are auto-detected** from modlist.txt structure
- **Handles MO2's reverse display order** correctly
- **Renames are NOT auto-detected** — they surface as a `-D` + `+E` pair (e.g. old `Milfactory Brelyna` removed, new `Milfactory - Mature College of Winterhold - Brelyna` added). Mark them as `M` manually in the changelog when you spot a rename.
- **Python scanner is reliable** - no more grep confusion issues

## Common Workflows

### Adding a New Mod
1. Identify appropriate category
2. Check dependencies and compatibility
3. Add entry to changelog with `+E ModName // Comment`
4. Note version number
5. Run relevant build tools
6. Test functionality

### Updating an Existing Mod
1. Find mod in changelog
2. Note current version
3. Add entry: `M ModName // Updated from X to Y`
4. Run relevant build tools if needed
5. Test for issues

### Checking for Available Mod Updates
**TRIGGER:** When user asks "what needs updating?", "check for updates", or similar.

MO2 caches each mod's latest Nexus version in its `meta.ini` (`newestVersion` field) when the user clicks **Check for Updates** in MO2. We can scan those to produce an update report.

**Step 1: Ask the user to refresh MO2's update cache**
- User should click the **Check all for updates** button (globe icon) in MO2 and wait for it to finish
- This updates the `newestVersion` field in every mod's `meta.ini`

**Step 2: Run the update scanner**
```python
python -c "
import os, configparser

mods_dir = 'D:/Modlists/Elden/mods'
updates = []

for entry in sorted(os.listdir(mods_dir)):
    ini_path = os.path.join(mods_dir, entry, 'meta.ini')
    if not os.path.isfile(ini_path):
        continue
    if 'separator' in entry.lower():
        continue
    
    config = configparser.ConfigParser(strict=False)
    try:
        config.read(ini_path, encoding='utf-8')
        version = config.get('General', 'version', fallback='').strip()
        newest = config.get('General', 'newestVersion', fallback='').strip()
    except Exception:
        continue
    
    if not version or not newest or version == newest:
        continue
    if newest in ('', '0', '0.0', '0.0.0', '0.0.0.0'):
        continue
    
    updates.append((entry, version, newest))

print(f'Found {len(updates)} mods with available updates:\n')
for name, cur, new in updates:
    print(f'  {name}')
    print(f'    {cur}  -->  {new}\n')
"
```

**Step 3: Filter out false positives**
Some version mismatches are NOT real updates:
- **Date-stamped versions** (`d2025.6.14.0`) — MO2 assigns these when the mod page has no proper version; the "newest" is often the Nexus version string which looks different but isn't newer
- **Installed > Newest** (e.g., `1.14.0` → `1.1.7`) — versioning scheme mismatch, not a downgrade
- **Build output folders** (17.x, 18.x) — these are our own outputs, not Nexus mods
- **Cosmetic suffix differences** (`2.3.0.0` vs `2.3.0.0a`) — may be trivial hotfixes

**Step 4: Present results to user**
- Group by priority: frameworks/core first, combat system, then everything else
- Flag major version jumps that could break things (especially OAR, BFCO, SPID)
- Note mods that will require rebuild steps (animations → Pandora, LODs → DynDOLOD, etc.)

### Uploading Build Outputs to Nexus Mods
**TRIGGER:** When user says "upload to nexus", "push to nexus", or after rebuilding tool outputs (Pandora, BodySlide, DynDOLOD, etc.)

Build outputs are uploaded to Nexus Mods via a self-hosted GitHub Actions workflow in the [elden-rim-together-resources](https://github.com/DJLegends1011/elden-rim-together-resources) repo.

**Available upload targets** (defined in `nexus-upload-list.txt`):
| Entry | Nexus File Group ID |
|---|---|
| 17.3 Bodyslide Output | 3111667 |
| 17.4 Pandora Output | 5765650 |
| 18.0 LODGen Output | 3111685 |
| 18.1 TexGen Output | 3111688 |
| 18.2 DynDOLOD Output | 3111691 |

**Prerequisites:**
- The self-hosted runner must be active. Check status with `gh api repos/DJLegends1011/elden-rim-together-resources/actions/runners` — look for `status=online`. If offline, launch `C:\Users\DJLegnds\Downloads\Mods\modpack updating\Start Nexus Runner.bat` (Claude can launch this directly via Bash with `cmd //c start "" "Start Nexus Runner.bat"`)
- The `NEXUSMODS_API_KEY` repo secret must be valid

**Upload a specific output:**
```bash
gh workflow run "Upload Elden Resources to Nexus Mods" \
  --repo DJLegends1011/elden-rim-together-resources \
  -f version="X.X.X" \
  -f description="Description of changes" \
  -f filter="17.4 Pandora Output" \
  -f dry_run=false
```

**Upload all outputs at once** (omit the filter):
```bash
gh workflow run "Upload Elden Resources to Nexus Mods" \
  --repo DJLegends1011/elden-rim-together-resources \
  -f version="X.X.X" \
  -f description="Description of changes" \
  -f filter="" \
  -f dry_run=false
```

**Dry run** (build archives only, no upload):
Set `-f dry_run=true`

**Check progress:**
```bash
gh run list --repo DJLegends1011/elden-rim-together-resources --limit 1
gh run view <run_id> --repo DJLegends1011/elden-rim-together-resources
```

**If upload fails with `fetch failed`:**
- Most likely the Nexus API key expired — user needs to regenerate at nexusmods.com and update the `NEXUSMODS_API_KEY` secret in repo settings
- Also check the Node.js deprecation warnings — the `Nexus-Mods/upload-action` may need updating

### Compiling the Wabbajack List (GUI only)
**TRIGGER:** When user says "compile the list", "build the wabbajack", or similar.

Compiling and publishing both happen through the **Wabbajack GUI** (settings: `D:\Modlists\Elden\EldenRim Together.compiler_settings`; the Publish button uploads to authored-files.wabbajack.org and writes the "New release" commit to `modlists.json`).

- **Close MO2 before compiling** — it holds `logs\fomodplus.log` locked and the compile crashes
- **dMenu must ship** — dMenu NG depends on it; players insta-CTD without it (it was wrongly in the GUI Ignore list until 06/12/2026)
- STR's embedded-browser cache (`mods\Skyrim Together Reborn\SkyrimTogetherReborn\cache`) regenerates every play session; the GUI Ignore list covers it — keep that entry when STR updates
- CLI compilation (`wabbajack-cli.exe compile`) was attempted and **removed** on 06/12/2026: it ignores the GUI settings file and needs marker files/meta.ini tags mirrored everywhere, and final exports kept dying on a deterministic network error. Full post-mortem lives in Claude's memory (`wabbajack-cli-compile`) — read it before ever re-attempting.

### Modular MO2 Dashboard (Startup Dashboard Plugin)

The modpack uses the **Modular MO2 Dashboard** plugin to let players configure graphics, UI, gamepad, NSFW, and other settings before launching the game.

**Plugin location:** `D:\Modlists\Elden\plugins\StartupDashboard`
**Backup location:** `C:\Users\DJLegnds\Downloads\Mods\modpack updating\startup dashboard backup`

**Key files:**
- `StartupDashboard.rules.json` — Defines all toggle rules (which mods to enable/disable per option: ENB vs Community Shaders, UI mods, DLSS, gamepad, etc.)
- `presets/` — User-facing preset configs. Format matches `_collect_state()` schema: combobox categories use string text, hardcoded checkboxes (dlss/nsfw/gamepad/poise/npc_resistances) use booleans, auto-discovered categories (parallax) use string text. Resolution omitted (auto-detected from monitor)
  - **Default.json** — NSFW On, Mortal Enemies On, DLSS On, Gamepad Off, Parallax Off
  - **Non_Gooner.json** — Same as Default but NSFW Off (SFW variant)
  - **Visuals_Max.json** — Same as Default but Parallax On (strong GPU)
  - **Controller.json** — Same as Default but Gamepad On (couch/Steam Deck)

**Backup routine:**
After modifying the dashboard rules or presets, copy the updated files to the backup folder:
```bash
cp "D:/Modlists/Elden/plugins/StartupDashboard/StartupDashboard.rules.json" "C:/Users/DJLegnds/Downloads/Mods/modpack updating/startup dashboard backup/"
cp -r "D:/Modlists/Elden/plugins/StartupDashboard/presets/"* "C:/Users/DJLegnds/Downloads/Mods/modpack updating/startup dashboard backup/presets/"
```

**Restore routine (after plugin update wipes configs):**
```bash
cp "C:/Users/DJLegnds/Downloads/Mods/modpack updating/startup dashboard backup/StartupDashboard.rules.json" "D:/Modlists/Elden/plugins/StartupDashboard/"
cp -r "C:/Users/DJLegnds/Downloads/Mods/modpack updating/startup dashboard backup/presets/"* "D:/Modlists/Elden/plugins/StartupDashboard/presets/"
```

**When to backup:** After any changes to rules.json or presets (new toggle options, new presets, renamed mods affecting rules)
**When to restore:** After updating the Modular MO2 Dashboard plugin from Nexus (updates overwrite configs)

**Known upstream plugin bugs (plugin v2026.01.15.v2 — reported upstream, awaiting fix):**
- **Hardcoded checkbox defaults ignored:** `defaults.nsfw/gamepad/poise/permadeath/npc_resistances` in rules.json don't affect the checkboxes on first dashboard open (`StartupDashboard.py:4452-4457` hardcodes initial states). **Workaround:** Tell players to click `Load preset → Default` after dashboard opens for the first time.
- **`reshade` and `map_type` can't be hidden:** Setting `ui_visibility.reshade = false` and `ui_visibility.map_type = false` has no effect because `_apply_ui_visibility` (line 5786) omits these combos from its hardcoded `combo_map`. They'll stay visible until upstream fix. They don't break anything — Reshade defaults to "Off", Map Type defaults to "Paper World Map (Default)".

**Configuration Editor:** Accessible from MO2 via the StartupDashboard plugin. Used to build `rules.json` visually — each tab corresponds to a rules section. Use "Add Option" to create dropdown choices or toggle states, mapping mod names to enable/disable lists.

**Rules.json — Current State (rewritten from scratch):**
Replaced the original Wunduniik proof-of-concept. Live file at `D:/Modlists/Elden/plugins/StartupDashboard/StartupDashboard.rules.json`, backed up to `startup dashboard backup/`.

**Active (visible) categories:**
- **Graphics Framework** — ENB (Default) — single option, bundles all ENB framework mods + entire 05.08 PARTICLE LIGHTS - ENB LIGHT section
- **ENB Preset** — RUDY NAT III ENB — single option (only preset installed)
- **DLSS** — On (default) / Off — toggles Frame Generation mods
- **UI Mod** — Oathvein UI — single option (Prisma is a framework, always on)
- **NSFW** — On (default) / Off — toggles TNG (male) + 5 BHUNP "milker" presets (Excessively Curvy, Critical Mass, D-sney Mommy, FantasyBody2, N55 Imperial Badonkas)
- **Gamepad** — Off (default) / On — toggles 4 gamepad mods together
- **Difficulty** — On (default) / Off — toggles Mortal Enemies + its Restless Dead SkyPatcher patch (Restless Dead itself is hardcoded always-on)
- **Resolution** — 9 buckets (720p–8K) as empty placeholders. Plugin still uses player's choice for `ResolutionScale` (SSE Display Tweaks) and aspect-ratio detection
- **Parallax** — Off (default) / On — auto-discovered custom category. On enables Skyland Whiterun/Landscapes Complex Parallax + Terrain Helper + Rudy ENB SE for Parallax (layered on top of Rudy NAT 3, not replacing it)

**Ultrawide handling (`ui_widescreen_overrides`):** Plugin auto-detects aspect ratio (16:9 / 21:9 / 32:9 etc.) and applies overrides per ratio. Currently wired:
- **21:9** → auto-enables `Oathvein UI - 219 Ultrawide Version` when Oathvein UI is the selected `ui_mod`
- **32:9** → stub present, no patches installed yet

**Hidden categories (`ui_visibility: false`, no real mods to toggle yet):**
main_menu, anti_aliasing, grass_type, ui_position, ini_base, npc_resistances, poise

**Future buildout TODO:**
- **Poise** — currently hidden; Maxsu Block Overhaul is behavior-based, not a true poise mod. Re-enable category if a real poise system is added (LOKI poise, etc.)
- **Resolution** — buckets are placeholders; add 2K/4K/8K texture pack tier toggles when tiered packs get installed
- **32:9 ultrawide** — no 32:9 patches installed yet; add to `ui_widescreen_overrides["32:9"]["ui_mod_patches"]` as they appear
- **INI Base** — Low/Med/High INI presets need INI file swapping (not mod toggles); implement via Papyrus Ini Manipulator if desired
- **NPC Resistances** — fold into Difficulty or expand with dedicated resistance mods
- **Grass Type** — only "Landscape Fixes For Grass Mods" infrastructure is present; add Folkvangr/Veydosebrom etc. to enable a toggle
- **Main Menu** — no replacer installed; add if desired

### Troubleshooting Crashes
1. Check SKSE version compatibility
2. Review recent changelog entries
3. Check for mod conflicts in category
4. Verify load order
5. Review crash logs
6. Test with problematic mods disabled

## Resources

- **Skyrim Together Reborn**: [GitHub](https://github.com/tiltedphoques/TiltedEvolution)
- **Mod Organizer 2**: [GitHub](https://github.com/ModOrganizer2/modorganizer)
- **Wabbajack**: [Website](https://www.wabbajack.org/)
- **SKSE**: [skse.silverlock.org](http://skse.silverlock.org/)

## Notes

- This modpack emphasizes Elden Ring-inspired combat via BFCO (Attack Behavior Framework) and Elden Parry
- Animation system uses OAR (Open Animation Replacer) and Pandora (Nemesis-compatible behavior engine)
- Heavy focus on visual enhancements while maintaining multiplayer stability
- Combat movesets include Elden Ring weapons: Katanas, Rapiers, Twinblades, Scythes
