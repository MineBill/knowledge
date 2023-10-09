# Allow flatpak applications to access system cursor themes
[keywords]: <> (linux flatpak theme cursor)

```sh
flatpak --user override --filesystem=/home/$USER/.icons/:ro
flatpak --user override --filesystem=/usr/share/icons/:ro
```

Make sure the `XCURSOR_PATH` environemnt variable is empty, check KDE System Settings:
> Applications > Flatpak Permission Settings > Discord > Environment