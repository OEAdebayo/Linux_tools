### Make desktop applications in Linux instead of running from the command line

Create a `.desktop` launcher file like this:
```bash
nano ~/.local/share/applications/<name of application>.desktop
```
or, if you want it to appear directly on your desktop:
```bash
nano ~/Desktop/<name of application>.desktop
```

Paste the following content (adjust the version and paths):

```ini
[Desktop Entry]
Type=Application
Name=<application name>
Comment=Launch <application name>
Exec=/usr/local/location/of/the/launcher/file -desktop
Icon=/location/of/the/application/icon.png
Terminal=false
Categories=Development;Education;Science;
StartupNotify=true
```

#### Note: Replace `/usr/local/location/of/the/launcher/file` with the actual application intall launcher directory or it won't work.

#### Make it executable

If you saved it in `~/Desktop`:

```bash
chmod +x ~/Desktop/< application name >.desktop
```

If you saved it in `~/.local/share/applications`:

```bash
chmod +x ~/.local/share/applications/< application name >.desktop
```
