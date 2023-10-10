# Building [Lightly](https://github.com/boehs/Lightly) on Fedora

Make sure to install all of the required and optional cmake dependencies, the optional are not optional:
```sh
sudo dnf install cmake extra-cmake-modules "cmake(Qt5Core)" "cmake(Qt5Gui)" "cmake(Qt5DBus)" "cmake(Qt5X11Extras)" "cmake(KF5GuiAddons)" "cmake(KF5WindowSystem)" "cmake(KF5I18n)" "cmake(KDecoration2)" "cmake(KF5CoreAddons)" "cmake(KF5ConfigWidgets)" "cmake(Qt5UiTools)" "cmake(KF5GlobalAccel)" "cmake(KF5IconThemes)" kwin-devel libepoxy-devel "cmake(KF5Init)" "cmake(KF5Crash)" "cmake(KF5KIO)" "cmake(KF5Notifications)" kf5-kpackage-devel "cmake(Qt5Quick)" "cmake(KF5FrameworkIntegration)" "cmake(KF5Wayland)" "cmake(KF5KCMUtils)" 
```
```sh
cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_LIBDIR=lib64 -DBUILD_TESTING=OFF ..
```
Also, change the `cmake_minimum_version` to `3.16.0`.