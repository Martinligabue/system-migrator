# System Migrator

## Overview
System Migrator is a GUI management tool to migrate data, programs and settings to a new system. The primary features it offers are:
* A clear and easy-to-use interface for backing up and restoring user data, including options for selecting specific files and directories to include in the backup.
* A way to save and restore system settings and configurations, such as desktop settings, program preferences, and custom scripts.
* A feature for saving and restoring auto-start programs and services, allowing users to easily add, remove, or modify programs that start automatically when the system boots up.
* A tool for managing Flatpak, Snap, and other application package formats, including options for backing up and restoring installed applications, as well as their configuration settings.
* (An interface for managing user permissions and access control, making it easy to manage which users can access which files and directories.
* A feature for saving and restoring network settings, including wireless network configurations and VPN connections.
* Optional: Saving states of the system

### Screenshots
![image](/uploads/21da59577c3e8a101347cf0d59569c09/image.png)

![image](/uploads/41aa431b6a0de85bc70b84d90da392ea/image.png)

![image](/uploads/65b6004c3257d66154828259a0fed47d/image.png)

![image](/uploads/d255a9d9839ba8633b8e911858f4b48f/image.png)

![image](/uploads/429be74e9fb92088697944d23a1def1d/image.png)

![image](/uploads/ea3940775576a3a0ef7f205b8f2fd77a/image.png)

## Installing

#### Arch
System Migrator can be installed from the AUR as `btrfs-assistant`

#### Debian/Ubuntu
1. Install the prerequisites: `sudo apt install git cmake qtbase5-dev qttools5-dev fonts-noto libqt5svg5 libqt5core5a g++ libbtrfs-dev libbtrfsutil-dev`
1. Download the tar.gz from the latest version [here](https://gitlab.com/btrfs-assistant/btrfs-assistant/-/tags)
1. Untar the archive and cd into the directory
1. `cmake -B build -S . -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE='Release'`
1. `make -C build`
1. `sudo make -C build install`
1. Optionally install Snapper - `sudo apt install snapper`

#### Fedora
1. Install the prerequisites: `sudo dnf install cmake git qt5-qttools qt5-qtbase qt5-qtsvg g++ qt5-qtbase-devel qt5-qttools-devel libbtrfsutil btrfs-progs-devel`
1. Download the tar.gz from the latest version [here](https://gitlab.com/btrfs-assistant/btrfs-assistant/-/tags)
1. Untar the archive and cd into the directory
1. `cmake -B build -S . -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE='Release'`
1. `make -C build`
1. `sudo make -C build install`
1. Optionally install Snapper - `sudo dnf install snapper`
1. Optionally install Btrfs Maintenance - `sudo dnf install btrfsmaintenance`
1. Configure Btrfs Maintenance if installed - Edit `/etc/btrfs-assistant.conf` and change `bm_config` to `/etc/sysconfig/btrfsmaintenance`

## Contributing
Contributions are welcome!

Please see [CONTRIBUTING.md](docs/CONTRIBUTING.md) for more details.


### Development Requirements
* Qt5 / Qt Design UI
* C++17
* Cmake >= 3.5
* Root user privileges
* Btrfs filesystem
