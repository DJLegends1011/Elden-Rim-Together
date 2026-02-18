# Elden Rim Together

![Elden Rim Together](modlist-image.png)

**A Skyrim Together Reborn Modpack**

Elden Rim Together is a comprehensive Skyrim Special Edition modpack that combines modern Elden Ring-inspired combat mechanics with full Skyrim Together Reborn multiplayer compatibility. Experience cooperative Skyrim with friends while enjoying cutting-edge combat animations, visual enhancements, and gameplay improvements.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Skyrim Together Reborn Setup](#skyrim-together-reborn-setup)
- [First Launch](#first-launch)
- [Common Issues & Troubleshooting](#common-issues--troubleshooting)
- [Mod Highlights](#mod-highlights)
- [Gameplay Tips](#gameplay-tips)
- [FAQ](#faq)
- [Support](#support)
- [Credits](#credits)

---

## Overview

**Current Version:** 3.3.0
**Last Updated:** February 17, 2026
**Wabbajack File:** `Elden Rim Together.wabbajack`
**Game Version:** Skyrim Special Edition 1.6.1170+
**Creation Club:** Compatible with the 4 FREE Creation Club items (Fishing, Rare Curios, Survival Mode, Saints & Seducers). NOT compatible with the full Anniversary Edition bundle.

This modpack has been in development for nearly six years, carefully testing and balancing hundreds of mods to create the ultimate cooperative Skyrim experience. Whether you're exploring dungeons with friends or taking on world bosses together, Elden Rim Together delivers modern combat mechanics while maintaining multiplayer stability.

### What Makes This Special?
- **Elden Ring Combat:** Full BFCO (Attack Behavior Framework) integration with Elden Ring movesets
- **Multiplayer Ready:** Every mod tested for Skyrim Together Reborn compatibility
- **Visual Overhaul:** 2K-4K textures, ENB, weather systems, and lighting improvements
- **Animation Overhaul:** 1000+ new animations via OAR (Open Animation Replacer)
- **Performance Balanced:** Optimized for stable 60 FPS on mid-range hardware

---

## Features

### Combat System
- **BFCO (Attack Behavior Framework)** - Elden Ring-style combat system
- **Elden Parry** - Precision parrying mechanics with riposte attacks
- **Precision** - Hitbox-based combat for skill-based gameplay
- **True Directional Movement** - Modern third-person combat controls
- **Weapon Movesets:**
  - Elden Ring Katanas (flowing, fast attacks)
  - Elden Ring Rapiers (thrust-focused combat)
  - Elden Ring Twinblades (dual-wielding spins)
  - Elden Ring Scythes (sweeping attacks)
  - Heavy Armory weapons (pikes, halberds, quarterstaves)

### Animation Overhaul
- **Vanargand Animations** - Modern one-handed and dual-wield combat
- **Leviathan Animations** - Weighty greatsword movesets
- **Goetia Animations** - Spell casting and staff animations
- **1000+ Custom Animations** - Idles, locomotion, interactions, gestures
- **Dynamic Animations** - Context-aware sitting, leaning, weather reactions

### Visual Enhancements
- **ENB:** Rudy ENB for NAT 3 (Natural and Atmospheric Tamriel)
- **Weather:** NAT 3 (Natural and Atmospheric Tamriel) with volumetric mists
- **Lighting:** Lux (interiors) + Lux Orbis (exteriors) + Lux Via (roads)
- **Textures:** 2K-4K with parallax support
- **Landscapes:** Enhanced grass, trees, mountains, and water
- **Architecture:** Complete city and dungeon retextures

### User Interface
- **SkyUI** - Modern inventory and menu system
- **TrueHUD** - Boss health bars and player status
- **Oathvein UI** - Stylized UI theme
- **Contextual Crosshair** - Dynamic interaction prompts
- **QuickLootIE** - Fallout 4-style looting
- **Compass Navigation Overhaul** - Improved navigation

### Gameplay Improvements
- **Experience (XP System)** - Level by exploring and completing quests
- **Survival Mode** - Survival Control Panel for needs management
- **Alternate Perspective** - Enhanced alternate start options
- **Static Skill Leveling** - Skills don't level from use (balanced for multiplayer)
- **Custom Skills Framework** - New skill trees and progression

### Skyrim Together Reborn
- **Full Compatibility** - All mods tested for multiplayer sync
- **Shared Quests** - Quest progression works cooperatively
- **Synced Combat** - Combat mechanics synchronized between players
- **Performance Optimized** - Stable multiplayer experience

---

## Requirements

### Hardware Requirements
**Minimum:**
- CPU: Intel i5-8400 / AMD Ryzen 5 2600
- GPU: NVIDIA GTX 1060 6GB / AMD RX 580 8GB
- RAM: 16 GB
- Storage: 150 GB free space (SSD strongly recommended)
- OS: Windows 10/11 64-bit

**Recommended:**
- CPU: Intel i7-9700K / AMD Ryzen 7 3700X
- GPU: NVIDIA RTX 2070 / AMD RX 5700 XT
- RAM: 32 GB
- Storage: 200 GB free space on SSD
- OS: Windows 10/11 64-bit

### Software Requirements
- **Skyrim Special Edition** (Steam version)
  - Version 1.6.1170 or newer
  - **IMPORTANT:** This modpack is designed for the BASE game with only the 4 FREE Creation Club items (Fishing, Rare Curios, Survival Mode, Saints & Seducers)
  - **NOT compatible** with the full Anniversary Edition upgrade bundle (100+ paid CC content)
  - A separate AE-compatible variant will be available in the future
- **Wabbajack** (latest version)
  - Download from: [wabbajack.org](https://www.wabbajack.org/)
- **Microsoft Visual C++ Redistributables**
  - [VC++ 2015-2022 x64](https://aka.ms/vs/17/release/vc_redist.x64.exe)
- **.NET Runtime 6.0+**
  - [.NET Desktop Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- **Nexus Mods Account**
  - Free account minimum
  - Premium recommended (for automatic downloads)

---

## Installation

### Step 1: Prepare Your System

1. **Clean Skyrim Installation (IMPORTANT)**
   ```
   - Uninstall Skyrim Special Edition via Steam
   - Delete: C:\Program Files (x86)\Steam\steamapps\common\Skyrim Special Edition
   - Delete: Documents\My Games\Skyrim Special Edition
   - Reinstall Skyrim via Steam
   - Launch Skyrim once from Steam to generate INI files
   - Close Skyrim after reaching the main menu
   ```

2. **Verify Game Version**
   - Right-click Skyrim in Steam → Properties → Local Files → Browse
   - Right-click `SkyrimSE.exe` → Properties → Details tab
   - Version should be 1.6.1170 or higher

3. **Disable Steam Cloud**
   - Right-click Skyrim in Steam → Properties → General
   - Uncheck "Keep game saves in the Steam Cloud"

### Step 2: Install Wabbajack

1. Download [Wabbajack](https://www.wabbajack.org/)
2. Create a folder: `C:\Wabbajack` (or any location **NOT** in Program Files)
3. Extract `Wabbajack.exe` to this folder
4. Run `Wabbajack.exe` as Administrator

### Step 3: Install Elden Rim Together

1. **Download the Modlist File**
   - Option A: In Wabbajack, click "Browse Modlists" and search for "Elden Rim Together"
   - Option B: Download `Elden Rim Together.wabbajack` from the [GitHub Releases](https://github.com/DJLegends1011/Elden-Rim-Together/releases)

2. **Configure Installation Paths**
   - **Installation Location:** `C:\Modlists\Elden Rim Together` (or any drive with enough space)
     - ⚠️ **NEVER** install to Program Files, Desktop, or Documents
     - ⚠️ **NEVER** install to the same drive as Skyrim if space is limited
   - **Download Location:** `C:\Modlists\Elden Rim Together\downloads` (or separate fast drive)

3. **Start Installation**
   - Click the play button in Wabbajack
   - If you have Nexus Premium: Downloads will be automatic (2-4 hours)
   - If you have Nexus Free: You'll need to manually click download for each mod (4-8 hours)

4. **Wait for Installation**
   - Total download size: ~80-100 GB
   - Installed size: ~150 GB
   - Installation time: 2-6 hours depending on internet speed and Nexus account type

5. **Installation Complete**
   - You'll see "Installation Complete" when finished
   - Do NOT close Wabbajack until you see this message

### Step 4: Post-Installation Setup

1. **Navigate to Installation Folder**
   - Go to: `C:\Modlists\Elden Rim Together` (or your chosen path)

2. **Create Desktop Shortcuts (Optional)**
   - Right-click `ModOrganizer.exe` → Send to → Desktop (create shortcut)

3. **IMPORTANT: Point Skyrim Together Reborn to Your Game**

   Skyrim Together Reborn is already included in the modpack, but needs to know where your Skyrim installation is located:

   - Launch Mod Organizer 2 (`ModOrganizer.exe`)
   - In the top-right dropdown, select **"SkyrimTogether"** from the profile list
   - **Hold the SPACEBAR** while clicking the **"Run"** button
   - A file browser will pop up asking for `SkyrimSE.exe`
   - Navigate to: `[Your Modpack Install]\Stock Game\SkyrimSE.exe`
     - Example: `C:\Modlists\Elden Rim Together\Stock Game\SkyrimSE.exe`
   - Select `SkyrimSE.exe` and click Open
   - **You only need to do this once** - it will remember the path

   **Why this is needed:** STR needs to point to the actual game executable in the Stock Game folder to launch properly.

---

## Skyrim Together Reborn Setup

**Good News:** Skyrim Together Reborn is already installed and configured in this modpack! You don't need to download or install anything separately.

### Playing Multiplayer

#### Option 1: Joining a Friend's Session

1. **Launch the Game**
   - In Mod Organizer 2, select **"SkyrimTogetherServer"** from the profile dropdown (top right)
   - Click **"Run"**
   - (Remember: If this is your first time, hold SPACEBAR when clicking Run to point it to the Stock Game folder - see Installation Step 3)

2. **In-Game Menu**
   - Press `Right Ctrl` to open Skyrim Together menu
   - Click "Connect"
   - Enter your friend's server address and port
   - Default port: `10578`

3. **Connection Format**
   - If your friend is hosting: `[Their IP Address]:10578`
   - Example: `192.168.1.100:10578` (local network) or `203.0.113.45:10578` (internet)

#### Option 2: Hosting Your Own Server

**Easy Method (Local Network / Same House):**

1. **Start Hosting**
   - Launch game via Mod Organizer 2 using the **"SkyrimTogetherServer"** profile
   - Press `Right Ctrl` for STR menu
   - Click "Host"
   - Note the port (default: 10578)

2. **Find Your Local IP**
   - Press `Windows Key + R`
   - Type `cmd` and press Enter
   - Type `ipconfig` and press Enter
   - Find "IPv4 Address" under your network adapter (looks like `192.168.x.x`)

3. **Share with Friends**
   - Give friends your IP and port: `192.168.1.100:10578`
   - They can connect if on the same network

**Advanced Method (Internet Play):**

1. **Port Forward on Your Router**
   - Open your router settings (usually `192.168.1.1` or `192.168.0.1` in browser)
   - Find "Port Forwarding" section
   - Create new rule:
     - **Service Name:** Skyrim Together
     - **Port:** 10578
     - **Protocol:** UDP
     - **Internal IP:** Your PC's local IP (from ipconfig above)
   - Save settings

2. **Find Your Public IP**
   - Visit: [whatismyipaddress.com](https://whatismyipaddress.com/)
   - Note your public IP address

3. **Firewall Exception**
   - Windows Security → Firewall & network protection → Advanced settings
   - Inbound Rules → New Rule → Port
   - UDP, Port 10578
   - Allow the connection
   - Name it "Skyrim Together Reborn"

4. **Start Hosting**
   - Launch game, press `Right Ctrl`, click "Host"
   - Give friends your public IP: `[Your Public IP]:10578`

**Easiest Method (For Non-Technical Users):**

Use a VPN service like **Hamachi** or **Radmin VPN**:
1. Download [Radmin VPN](https://www.radmin-vpn.com/) (free, no limits)
2. Create a network or join friend's network
3. Use the Radmin VPN IP address to connect
4. No port forwarding needed!

### Multiplayer Tips

- **Save Often:** Desyncs can happen, save frequently
- **Quest Progress:** Some quests work better when done together
- **Load Order:** All players must have identical mod load orders
- **Version Matching:** Everyone must use the same modlist version
- **Server Host:** The host should have the best internet connection

---

## First Launch

### Initial Setup Checklist

1. **Launch Mod Organizer 2**
   - Run `ModOrganizer.exe` from your installation folder
   - Select "SKSE" from the dropdown (top right)
   - Click "Run"

2. **Wait for Initial Load**
   - First launch takes 3-5 minutes
   - SKSE and scripts are loading
   - You'll see "SKSE64 loaded successfully" in top-left corner

3. **MCM Configuration**
   - Press `Escape` → Mod Configuration
   - **Auto Saver:** Configured to save after combat ends (not at combat start)
   - **TrueHUD:** Customize boss bar position
   - **SkyUI:** Configure inventory preferences
   - **Experience:** Adjust XP gain rates if desired

4. **Graphics Settings**
   - Press `Escape` → Settings → Display
   - **Recommended Settings:**
     - Resolution: Your native resolution
     - Display Mode: Borderless Window
     - VSync: Off (ENB handles frame limiting)
     - TAA: On

5. **Control Bindings**
   - See `Control Bindings.md` in the GitHub repository
   - **Key Bindings:**
     - `Right Ctrl` - Skyrim Together Reborn menu
     - `C` - Character menu
     - `Tab` - Inventory
     - `M` - Map
     - `K` - Skills
     - `J` - Journal

6. **Create Character**
   - Choose "Alternate Perspective" start
   - Full customization with RaceMenu
   - Start location options available

7. **Test Run**
   - Walk around the starting area
   - Test combat with basic enemies
   - Check FPS (use ENB FPS counter: `Shift + Enter`)
   - Save your game

---

## Common Issues & Troubleshooting

### "Can't find SkyrimSE.exe" or Skyrim Together Won't Launch

**Problem:** STR won't launch or says it can't find the game

**Solution:**
This is usually because you haven't pointed STR to your game executable yet.

1. Open Mod Organizer 2
2. Select **"SkyrimTogetherServer"** from the profile dropdown (top-right)
3. **Hold SPACEBAR** while clicking the **"Run"** button
4. When the file browser appears, navigate to: `[Your Install]\Stock Game\SkyrimSE.exe`
   - Example: `C:\Modlists\Elden Rim Together\Stock Game\SkyrimSE.exe`
5. Select the exe and click Open
6. Try launching again (this time without holding spacebar)

**Why this happens:** STR needs to know where the game executable is located on first launch.

---

### Game Crashes on Startup

**Problem:** Game crashes immediately or at logo screen

**Possible Solutions:**

1. **Verify SKSE Launch**
   - Always launch via Mod Organizer 2 → "SKSE" → Run
   - NEVER launch from Steam or desktop shortcut

2. **Check Antivirus**
   - Add Mod Organizer 2 folder to antivirus exceptions
   - Add Skyrim folder to antivirus exceptions
   - Some antivirus programs block SKSE DLL files

3. **Graphics Driver**
   - Update to latest NVIDIA or AMD drivers
   - NVIDIA: [nvidia.com/drivers](https://www.nvidia.com/Download/index.aspx)
   - AMD: [amd.com/support](https://www.amd.com/en/support)

4. **ENB Files**
   - If using NVIDIA 10-series or older, try disabling ENB:
   - In Mod Organizer 2, disable "ENB" and "Rudy ENB" mods
   - Launch game and see if it loads

5. **Check Install**
   - In Wabbajack, click "Install from Disk"
   - Point to your installation folder
   - Click "Verify" to check for corruption

---

### Infinite Loading Screen

**Problem:** Stuck on loading screen forever

**Solutions:**

1. **First Time Load**
   - First load always takes 3-5 minutes
   - Wait patiently, don't close the game

2. **New Game Issues**
   - Start new game, wait at initial loading screen
   - After 5 minutes, if still loading, close game
   - Delete: `Documents\My Games\Skyrim Special Edition\Saves`
   - Try again

3. **Missing Masters**
   - In Mod Organizer 2, check for red ⚠️ icons
   - Right pane should show no missing plugins
   - If missing, reinstall the modlist

4. **Too Many Saves**
   - Delete old saves from: `[Elden Rim Together Install]\profiles\Elden Rim Together\saves`
   - Keep only recent 10-20 saves

---

### Low FPS / Performance Issues

**Problem:** Game runs below 30 FPS

**Solutions:**

1. **Reduce ENB Effects**
   - In-game, press `Shift + Enter` (ENB menu)
   - Disable expensive effects:
     - Subsurface Scattering → Off
     - Complex Fire Lights → Off
     - Detailed Shadow → Off

2. **Lower Grass Density**
   - In Mod Organizer 2, edit `SkyrimPrefs.ini`
   - Find: `iMinGrassSize=`
   - Change value to 60 or 80 (higher = less grass)

3. **DynDOLOD Performance**
   - In Mod Organizer 2, disable "DynDOLOD Output"
   - This removes distant object detail but improves FPS

4. **Resolution Scaling**
   - In ENB menu (`Shift + Enter`)
   - Change "Resolution Scale" to 0.85 or 0.75

5. **Background Programs**
   - Close Discord overlay, Xbox Game Bar, GeForce Experience overlay
   - These can cause stuttering

---

### Skyrim Together Connection Issues

**Problem:** Can't connect to friend's server

**Solutions:**

1. **Firewall Blocking**
   - Windows Security → Firewall & network protection → Allow an app
   - Add `SkyrimSE.exe` from your Skyrim installation
   - Allow both Private and Public networks

2. **Port Not Open**
   - Verify host has port forwarded 10578 (UDP)
   - Use [canyouseeme.org](https://canyouseeme.org/) to test port
   - Enter 10578 and check

3. **Wrong IP Address**
   - Local network: Use local IP (192.168.x.x)
   - Internet: Use public IP (check whatismyipaddress.com)
   - Make sure to include port: `IP:10578`

4. **Version Mismatch**
   - ALL players must have identical Elden Rim Together version
   - Check your version in Mod Organizer 2 title bar
   - Reinstall if versions don't match

5. **Try VPN Method**
   - Use Radmin VPN or Hamachi (see Multiplayer section)
   - Simplest solution for non-technical users

---

### Missing Textures / Purple Objects

**Problem:** Objects are purple or have missing textures

**Solution:**
- This indicates incomplete installation
- Rerun Wabbajack installation
- Check that all downloads completed successfully
- Some mods may have failed to download

---

### "Failed to initialize renderer" Error

**Problem:** ENB won't initialize

**Solutions:**

1. **DirectX Issue**
   - Install: [DirectX End-User Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=35)
   - Restart PC

2. **Wrong ENB Version**
   - The modlist includes correct ENB version
   - Don't manually install ENB on top

3. **Integrated Graphics**
   - Make sure Skyrim uses dedicated GPU, not integrated graphics
   - NVIDIA Control Panel → Manage 3D Settings → Program Settings
   - Add SkyrimSE.exe → Select "High-performance NVIDIA processor"

---

### Controls Not Working / Keybinds Wrong

**Problem:** Controls don't match documentation

**Solution:**
- Check `Control Bindings.md` in the GitHub repository
- Reset controls in-game:
  - Settings → Controls → Reset to Defaults
  - Or download the control preset from the repository

---

### Crashes in Specific Locations

**Problem:** Game crashes consistently in certain areas

**Solutions:**

1. **Update Mods**
   - Check GitHub for modlist updates
   - Some crashes are fixed in newer versions

2. **Disable Mods Temporarily**
   - In Mod Organizer 2, disable mods one by one
   - Test the problem area after each disable
   - Identify the problematic mod

3. **Report the Issue**
   - Join the Discord server
   - Report the location and circumstances
   - Provide crash log from: `Documents\My Games\Skyrim Special Edition\SKSE`

---

## Mod Highlights

### Core Frameworks
- **SKSE64** - Script Extender (required for most mods)
- **SkyUI** - Modern UI overhaul
- **Address Library** - Plugin version compatibility
- **Engine Fixes** - Core bug fixes
- **powerofthree's Papyrus Extender** - Extended scripting
- **Keyword Item Distributor (KID)** - Dynamic item distribution
- **Spell Perk Item Distributor (SPID)** - Dynamic spell/perk distribution
- **Base Object Swapper (BOS)** - Dynamic object replacement
- **Open Animation Replacer (OAR)** - Animation framework

### Combat & Animations
- **BFCO (Attack Behavior Framework)** - Modern combat system
- **Elden Parry** - Parrying mechanics
- **Precision** - Hitbox collision
- **Precision Creatures** - Extended creature hitboxes
- **True Directional Movement** - Modern movement
- **Vanargand Animations** - One-handed/dual wield combat
- **Leviathan Animations** - Greatsword combat
- **Goetia Animations** - Magic casting
- **ADXP MCO BFCO Elden Ring Movesets** - Katana, rapier, twinblade, scythe
- **Nemesis** - Animation engine

### Visual Overhaul
- **ENB** - Post-processing effects
- **Rudy ENB for NAT 3** - ENB preset
- **NAT 3 (Natural and Atmospheric Tamriel)** - Weather system with volumetric effects
- **Lux** - Interior lighting
- **Lux Orbis** - Exterior lighting
- **Lux Via** - Road lighting
- **Majestic Mountains** - Mountain textures
- **Noble Skyrim** - Architecture retexture
- **Skyrim 3D Landscapes** - 3D landscape objects
- **Folkvangr Grass** - Grass overhaul
- **Enhanced Landscapes** - Landscape improvements
- **Realistic Water Two** - Water overhaul

### Gameplay Overhaul
- **Experience** - XP-based leveling system
- **Static Skill Leveling** - Skills don't level from use
- **Custom Skills Framework** - New skill trees
- **Survival Control Panel** - Survival mode management
- **Alternate Perspective** - Alternate start mod
- **Heavy Armory** - New weapon types

### UI & HUD
- **SkyUI** - Inventory overhaul
- **TrueHUD** - Boss bars
- **SkyHUD** - Customizable HUD
- **Compass Navigation Overhaul** - Improved compass
- **QuickLootIE** - Quick looting
- **Contextual Crosshair** - Dynamic crosshair
- **Oathvein UI** - UI theme
- **Wheeler** - Equipment wheel

### Quality of Life
- **Better Jumping** - Jump height improvements
- **Auto Input Switch** - Gamepad/keyboard auto-switch
- **SmoothCam** - Third-person camera
- **Favorite Misc Items** - Favorite system expansion
- **Better Third Person Selection** - Improved object selection
- **Regional Save Names** - Location-based save names

### Multiplayer
- **Skyrim Together Reborn** - Multiplayer mod
- **Skyrim Together Reborn Features Integration** - Compatibility patches

---

## Gameplay Tips

### Combat Tips
1. **Learn to Parry:** Elden Parry is powerful but requires timing
2. **Stamina Management:** All attacks cost stamina, manage carefully
3. **Weapon Choice:** Different weapons have different movesets
4. **Power Attacks:** Hold attack button for special moves
5. **Positioning:** True Directional Movement allows strafing and backpedaling

### Multiplayer Tips
1. **Stay Close:** STR works best when players stay near each other
2. **Quest Coordination:** Complete quest objectives together
3. **Loot Sharing:** Containers respawn for each player
4. **Fast Travel:** Works in multiplayer, coordinate before traveling
5. **Combat Sync:** Host should initiate combat when possible

### Performance Tips
1. **Save Regularly:** Before entering new areas or dungeons
2. **Limit Saves:** Keep only recent 20 saves
3. **Close Background Apps:** Discord overlay, GeForce Experience, etc.
4. **Monitor Temps:** Keep GPU under 80°C
5. **Update Drivers:** Keep graphics drivers current

### Progression Tips
1. **Experience System:** Level by exploring and completing objectives
2. **Skill Books:** Major source of skill levels
3. **Training:** Find trainers to level skills
4. **Survival Mode:** Optional but recommended for immersion
5. **Take It Slow:** Enjoy the enhanced graphics and animations

---

## FAQ

**Q: Can I add my own mods?**
A: Not recommended. The modlist is carefully balanced for multiplayer. Adding mods may cause desyncs or crashes.

**Q: Can I remove mods I don't like?**
A: Some mods can be safely disabled (visual mods mostly), but removing gameplay mods will break things. Ask in Discord first.

**Q: Does everyone need the same mods for multiplayer?**
A: Yes, all players must have identical mod load orders for STR to work properly.

**Q: Can I use old saves?**
A: No, you must start a new game with this modlist. Old saves will crash.

**Q: How do I update the modlist?**
A: Rerun Wabbajack with the new modlist file. It will only download changed files.

**Q: Can I use this without multiplayer?**
A: Absolutely! The modlist works great for single-player.

**Q: Is Creation Club content required?**
A: Only the 4 FREE Creation Club items are compatible (Fishing, Rare Curios, Survival Mode, Saints & Seducers). The full Anniversary Edition upgrade bundle (100+ paid CC content) is NOT compatible with this version. An AE variant is planned for the future.

**Q: Can I change the ENB preset?**
A: Yes, but performance and appearance may vary. Rudy ENB for NAT 3 is optimized for this modlist.

**Q: Why is my character moving slowly?**
A: Check if Survival Mode is enabled. It affects carry weight and speed.

**Q: Can I use controllers?**
A: Yes, full controller support is included with custom bindings.

---

## Support

### Official Discord
Join the **Elden Rim Together Discord** for:
- Installation help
- Troubleshooting support
- Multiplayer coordination
- Update announcements
- Community gameplay

**Discord Server:** https://discord.gg/YwU4dF2X9V

### GitHub
- **Issues:** [Report bugs](https://github.com/DJLegends1011/Elden-Rim-Together/issues)
- **Changelog:** [View version history](https://github.com/DJLegends1011/Elden-Rim-Together/blob/main/Changelog)
- **Documentation:** [Additional guides](https://github.com/DJLegends1011/Elden-Rim-Together)

### Useful Resources
- **Wabbajack:** [wabbajack.org](https://www.wabbajack.org/)
- **Skyrim Together Reborn:** [GitHub](https://github.com/tiltedphoques/TiltedEvolution)
- **SKSE:** [skse.silverlock.org](http://skse.silverlock.org/)
- **Nexus Mods:** [nexusmods.com/skyrimspecialedition](https://www.nexusmods.com/skyrimspecialedition)

---

## Credits

### Modlist Author
**DJLegends1011** - Creator and maintainer of Elden Rim Together

### Special Thanks
- **Skyrim Together Reborn Team** - For making multiplayer Skyrim possible
- **Wabbajack Team** - For the automated modlist installer
- **SKSE Team** - For the Script Extender
- **All Mod Authors** - For creating the incredible mods that make this possible

### Major Contributors
This modlist includes hundreds of mods from talented creators. Full credits available in Mod Organizer 2.

### Community
Thank you to everyone in the Discord community for testing, feedback, and support throughout development.

---

## License

This modlist is provided free of charge for personal use. All mods remain the property of their original creators. Please support mod authors by endorsing their work on Nexus Mods.

**Do not:**
- Reupload this modlist without permission
- Claim this modlist as your own work
- Use this modlist for commercial purposes

---

**Enjoy your journey through Skyrim with friends!**

*Last Updated: February 17, 2026*
*Version: 3.3.0*