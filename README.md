![](https://gitlab.com/arcmenu/arcmenu-assets/raw/master/images/azTaskbar.png)

---

### Introduction

YarlOS Taskbar is a simple taskbar extension for GNOME Shell, designed to provide a more familiar user experience and workflow. This extension places app icons in the panel showing current running apps, and GNOME favorites.

Modification Notice: This package is a downstream-modified build of the upstream azTaskbar extension. The changes may differ from the upstream project. The upstream license and copyright notices remain in effect.

Picture shown above uses [ArcMenu](https://extensions.gnome.org/extension/3628/arcmenu/) to add an application menu to the panel.

---

### Installation

#### Dependencies

Before installing, make sure the following tools are available on your system:

- `git`
- `make`
- `glib-compile-schemas`
- `gnome-extensions`
- `gettext` (for localization support, if you want to build translations)

#### Manual Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yarlos-project/yarlos-taskbar.git
   cd yarlos-taskbar
   ```

2. **Build the extension:**

   ```bash
   make
   ```

3. **Install the extension:**

   ```bash
   make install
   ```

4. **Enable the extension:**

   ```bash
   make enable
   ```

5. **Restart GNOME Shell:**
   - Press `Alt+F2`, type `r`, and press Enter
   - Or log out and log back in

---

### Credits

YarlOS Taskbar is maintained by the YarlOS Project.

**Original Credits**

- Significant portions of this project are heavily based on code from [Dash to Panel](https://github.com/home-sweet-gnome/dash-to-panel) and [Dash to Dock](https://github.com/micheleg/dash-to-dock)
  - Window Previews - Dash to Dock
  - UnityLauncherAPI - Dash to Dock
  - Notifications Monitor - Dash to Dock
  - Urgent Window Logic - Dash to Dock
  - AppIcon Mouse Scroll Cycle Window Logic - Dash to Panel
  - Window Peeking Feature - Dash to Panel
  - Intellihide and Proximity - Dash to Panel
- Panel Location feature based on code from Just Perfection extension

**Original Project**

- @[AndrewZaech](https://gitlab.com/AndrewZaech) - Original Project Maintainer and Developer

---

### Contributors

**YarlOS Taskbar**

- Maintained by [yarlos-project](https://github.com/yarlos-project)

**Original App Icons Taskbar Contributors**

**Logo**
Created by @[AndyC](https://gitlab.com/LinxGem33) and licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

**Code Contributions**
@[wednesbunny](https://gitlab.com/wednesbunny) !3 | @[Finnerale](https://gitlab.com/Finnerale) !13 | @[EmilyisWIP](https://gitlab.com/emilyiswip) !15 |
@[tmikaeld](https://gitlab.com/tmikaeld) !41

**Translators**

| Language             | Translators                                                                  |
| -------------------- | ---------------------------------------------------------------------------- |
| Brazilian Portuguese | @[Ian Almeida](https://gitlab.com/mr_yoshi)                                  |
| Dutch                | @[Vistaus](https://gitlab.com/Vistaus)                                       |
| French               | @[celeri](https://gitlab.com/celestomm)                                      |
| German               | @[daPhipz](https://gitlab.com/daPhipz), @[Etamuk](https://gitlab.com/Etamuk) |
| Hungarian            | @[Pummerp](https://gitlab.com/Pummerp)                                       |
| Polish               | @[MrCzwartek](https://gitlab.com/MrCzwartek)                                 |
| Russian              | @[Ser82-png ](https://gitlab.com/Ser82-png)                                  |
| Spanish              | @[Martin Torres](https://gitlab.com/martttin)                                |
| Swedish              | @[tmikaeld](https://gitlab.com/tmikaeld)                                     |

---
