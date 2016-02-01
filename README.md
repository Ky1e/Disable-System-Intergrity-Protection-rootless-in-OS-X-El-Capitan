# Disable-System-Intergrity-Protection-rootless-in-OS-X-El-Capitan

## Disabling Rootless on OS X El Capitan

### Info:

System Integrity Protection locks you out of the following directories until disabled:

<code>/System</code>

<code>/sbin</code>

<code>/usr (except /usr/local subdirectory)</code>

### Turning it off
1. Reboot your Mac and hold down <code>Command + R</code> together after you hear the boot sound. This will boot you into Recovery Mode.

2. Go to the top menu bar and select the Utilities dropdown menu and open Terminal.
3. Type the following and your Mac will automatically reboot:

    ```bash
$ csrutil disable; reboot
```

4. Once rebooted open Terminal and type the following to ensure it was disabled:

    ```bash
$ csrutil status
```

5. It should say:

    ```bash
$ csrutil status
System Integrity Protection status: disabled
```
