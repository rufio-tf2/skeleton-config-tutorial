# Skeleton Config

<table>
  <tr>
    <td>
      <h2>Table of Contents</h2>
      <ul>
        <li>
          <a href="#what-you-get">What you get</a>
          <ul>
            <li><a href="https://github.com/rufio-tf2/rufio-config/blob/master/cfg/actions.cfg">Additional actions</a></li>
            <li><a href="https://github.com/rufio-tf2/rufio-config/blob/master/cfg/settings.cfg">Improved settings</a></li>
            <li><a href="#shift-modifiers-arrow_upper_right">Shift-modifiers</a></li>
            <li><a href="#weapon-slot-settings-arrow_upper_right">Weapon-slot settings</a></li>
            <li><a href="#quick-loadout-switch-arrow_upper_right">Quick loadout switch</a></li>
            <li><a href="#quick-class-switch-arrow_upper_right">Quick class switch</a></li>
          </ul>
        </li>
        <li><a href="#download-arrow_double_down">Download</a></li>
        <li><a href="#install">Install</a></li>
        <li><a href="#uninstall">Uninstall</a></li>
        <li><a href="#contributing">Contributing</a></li>
      </ul>
    </td>
    <td><img src="./images/skeleton_smoking.png" alt="Skeleton Smoking" height="400px" width="302px" /></td>
  </tr>
</table>

> **_I recommend that you [install](#install) this Skeleton Config, and then add the features that you want. To see my config and how I'm using this skeleton, [click here](https://github.com/rufio-tf2/rufio-config)._**

## What you get

This is not an [FPS config](https://github.com/mastercoms/mastercomfig). This config is a framework that provides missing features to TF2:

- [Additional actions](https://github.com/rufio-tf2/rufio-config/blob/master/cfg/actions.cfg) (e.g. `alertSniper`, `alertSpyOnEngi`)
- [Improved settings](https://github.com/rufio-tf2/rufio-config/blob/master/cfg/settings.cfg) (e.g. interp, fov, and crosshair)
- [Modules](./cfg/modules/README.md):
  - _[Shift-modifiers](#shift-modifiers-arrow_upper_right):_ <kbd>SHIFT</kbd>+<kbd>MOUSE1</kbd>
  - _[Weapon-slot settings](#weapon-slot-settings-arrow_upper_right)_
  - _[Quick loadout switch](#quick-loadout-switch-arrow_upper_right):_ <kbd>&larr;</kbd><kbd>&uarr;</kbd><kbd>&rarr;</kbd><kbd>&darr;</kbd>
  - _[Quick class switch](#quick-class-switch-arrow_upper_right):_ <kbd>KEYPAD 1</kbd>-<kbd>9</kbd>

You should be able to swap in and out different parts of this config and customize the specifics.

### Shift-modifiers ([:arrow_upper_right:](https://github.com/rufio-tf2/key-modifiers))

These are some of shift actions that I use. For a more full explanation of how to work with these, read [this](https://github.com/rufio-tf2/key-modifiers).

- <kbd>SHIFT</kbd>+<kbd>MOUSE1</kbd> -- _Alert Spy_
- <kbd>SHIFT</kbd>+<kbd>MOUSE2</kbd> -- _Alert Sniper ahead_
- <kbd>SHIFT</kbd>+<kbd>MOUSE3</kbd> -- _Alert Spy is sapping engineer's buildings_
- <kbd>SHIFT</kbd>+<kbd>MWHEELUP</kbd> -- _Alert Incoming_
- <kbd>SHIFT</kbd>+<kbd>MWHEELDOWN</kbd> -- _Alert Incoming from behind_

#### Class-specific shift-modifiers

You can define class-specific versions of these modifiers for your customization pleasure :beers:

For example, on Spy I have <kbd>MOUSE4</kbd> execute the `lastdisguise` command, but on Pyro <kbd>MOUSE4</kbd> does a `detonatorJump`. You can create shift-modified versions of these. I define these class-specific overrides in that class's `key_modifiers.cfg` file.

Here are some class-specific overrides I've used:

<details>
  <summary>Engineer</summary>
  <ul>
    <li>
      <kbd>MOUSE3</kbd> -- <em>Destroy sentry and build</em>
    </li>
    <li>
      <a href="https://github.com/rufio-tf2/rufio-config/blob/master/cfg/classes/engineer/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

<details>
  <summary>Pyro</summary>
  <ul>
    <li>
      <kbd>MOUSE4</kbd> -- <em>Detonator jump</em>
    </li>
    <li>
      <a href="https://github.com/rufio-tf2/rufio-config/blob/master/cfg/classes/pyro/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>

</details>

<details>
  <summary>Soldier</summary>
  <ul>
    <li>
      <kbd>MOUSE4</kbd> -- <em>Rocket jump</em>
    </li>
    <li>
      I don't use this anymore, so I've commented this out (by adding two slashes). If you want to use it, remove the `//` from Line 4 and Line 7.
    </li>
    <li>
      <a href="https://github.com/rufio-tf2/rufio-config/blob/master/cfg/classes/soldier/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

<details>
  <summary>Spy</summary>
  <ul>
    <li>
      <kbd>MOUSE4</kbd> -- <em>Last diguise</em>
    </li>
    <li>
      <a href="https://github.com/rufio-tf2/rufio-config/blob/master/cfg/classes/spy/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

### Weapon-slot settings ([:arrow_upper_right:](https://github.com/rufio-tf2/weapon-slot-settings))

This lets you load settings per weapon slot. For example, you could:

- Change the crosshair color for different slots like [Mr. Slin does](https://github.com/misterslin/CrosshairSwitcher)
- Use it to turn the viewmodel on/off for certain slots
- Etc.

#### Class-specific weapon-slot settings

In the previous example, I established base slot-settings for all of the classes. But you can also create class-specific slot overrides. I put those settings in a class's `key_modifiers.cfg` file.

For example, I've previously used these viewmodel slot settings for different classes:

<details>
  <summary>Engineer</summary>
  <li>
    <code>tf/custom/skeleton-config/cfg/classes/engineer/weapon_slot_settings.cfg</code>
  </li>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
      <th>Slot 4</th>
      <th>Slot 5</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

<details>
  <summary>Scout</summary>
  <li>
    <code>tf/custom/skeleton-config/cfg/classes/scout/weapon_slot_settings.cfg</code>
  </li>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

<details>
  <summary>Soldier</summary>
  <li>
    <code>tf/custom/skeleton-config/cfg/classes/soldier/weapon_slot_settings.cfg</code>
  </li>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

<details>
  <summary>Spy</summary>
  <li>
    <code>tf/custom/skeleton-config/cfg/classes/spy/weapon_slot_settings.cfg</code>
  </li>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
      <th>Slot 4</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

### Quick loadout switch ([:arrow_upper_right:](https://github.com/rufio-tf2/quick-loadout-switch))

<details>
  <summary>Use the arrow keys to change your loadout.</summary>
  <ul>
    <li>:arrow_left: Loadout A</li>
    <li>:arrow_up: Loadout B</li>
    <li>:arrow_right: Loadout C</li>
    <li>:arrow_down: Loadout D</li>
  </ul>
</details>

I also have <kbd>ALT</kbd> bound to switch to Loadout A for quick resupply.

### Quick class switch ([:arrow_upper_right:](https://github.com/rufio-tf2/quick-class-switch))

<details>
  <summary>Use the numpad numbers to change your class.</summary>
  <ol>
    <li>Scout</li>
    <li>Soldier</li>
    <li>Pyro</li>
    <li>Demo</li>
    <li>Heavy</li>
    <li>Engineer</li>
    <li>Medic</li>
    <li>Sniper</li>
    <li>Spy</li>
  </ol>
</details>

## Download [[:arrow_double_down:](https://github.com/rufio-tf2/skeleton-config/archive/master.zip)]

If the link doesn't work, click the green "Clone or download" button on the top right of this page and click "Download ZIP".

<img src="https://i.imgur.com/OX9A0dt.png" width="50%" height="50%" alt="Download ZIP">

1.  Unzip my config to its own folder.
1.  Rename the config folder from `skeleton-config-master` to `skeleton-config`. (`master` is the [branch](https://guides.github.com/introduction/flow/))

## Install

Navigate to your `tf` folder. If you've chosen a custom location for your Steam folder, then you know where it is. If you used the default install path, then it should be:

- Windows: `C:\Program Files (x86)\Steam\steamapps\common\Team Fortress 2\tf\`
- macOS: `~/Library/Application Support/Steam/SteamApps/common/team fortress 2/tf/`
- Linux: `~/.steam/steam/SteamApps/common/Team Fortress 2/tf/`

You can also:

1.  Right click TF2 in your Steam library
1.  Click Properties
1.  Go to the "Local Files" tab
1.  Click the "Browse Local Files..." button
1.  Open the `tf` folder

### 1. Back up your current settings

I recommend [making a backup](./BACKUP.md) of your current settings in case you want to revert to your current setup. Also, remove any other configs you've got in place. You can even back up your whole `tf` folder if you want, it isn't that large.

### 2. Move config files

To install my files, open the `custom` folder that's inside of the `tf` folder. If `custom` doesn't exist, just create it.

1.  Navigate into `tf/custom/`
1.  Move `skeleton-config` into here

You should now have my config located at `tf/custom/skeleton-config`. Restart TF2 and everything should be setup.

**Note**: If anything is wonky after you install my config, please [let me know](https://github.com/rufio-tf2/skeleton-config/issues/new).

## Uninstall

Did you try out my config but want to revert to your backup? Read [this](./UNINSTALL.md).

## Contributing

You can always fork and edit. If you notice better ways that I could be doing things, I welcome pull requests.

## Thanks

Thanks to the community. This scripting takes getting used to, and I'm still figuring out the nuances. I couldn't have gotten into it if you all weren't posting your scripts.

## License

[MIT](./LICENSE.txt)
