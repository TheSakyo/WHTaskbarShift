# Taskbar Monitor Switcher

> **Fork** of [Primary taskbar on secondary monitor](https://windhawk.net/mods/taskbar-primary-on-secondary-monitor) 
> by **m417z**.
> All original features are preserved; a **keyboard shortcut** has been added.
>
> 📂 **Included in [Windhawk Mods Collection](https://github.com/TheSakyo/windhawk-mods)**

Move the primary taskbar — including tray icons, notifications, action center,
etc. — to another monitor.

The active monitor can be switched in three ways:
- **Settings** — pick a monitor by number or interface name (all versions).
- **Click** — double-click or middle-click the taskbar's empty space (Windows 11 only).
- **Keyboard shortcut** — press a configurable hotkey to instantly move the
taskbar to whichever monitor the mouse cursor is on.

![Demonstration](https://i.imgur.com/hFU9oyK.gif)

## Selecting a monitor

### By monitor number

Set the **Monitor** setting to the desired monitor number (1, 2, 3 …). Note
that this number may differ from the number shown in Windows Display Settings.

### By interface name

If monitor numbers change frequently (e.g. after locking your PC or restarting),
use the monitor's interface name instead. To find it:

1. Go to the mod's **Advanced** tab.
2. Set **Debug logging** to **Mod logs**.
3. Click **Show log output**.
4. Enter any text (e.g. `TEST`) in the **Monitor interface name** field and save.
5. In the log, look for lines like:
```
Found display device \\.\DISPLAY1, interface name: \\?\DISPLAY#DELA1D2#5&abc123#0#{e6f07b5f-…}
Found display device \\.\DISPLAY2, interface name: \\?\DISPLAY#GSM5B09#4&def456#0#{e6f07b5f-…}
```
6. Copy the relevant interface name (or a unique substring) into the
**Monitor interface name** setting.
7. Set **Debug logging** back to **None** when done.

**Monitor interface name** takes priority over the **Monitor** number when both
are set.

## Keyboard shortcut

When a keyboard shortcut is configured, pressing it moves the primary taskbar to
the monitor under the mouse cursor. If the cursor is **already on the taskbar's
monitor**, the shortcut is silently ignored — no unintended jumps.
