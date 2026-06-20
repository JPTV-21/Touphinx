# Touphinx
A patch for Dolphin that restores intuitive touchscreen behavior — long press for context menu, just like it should be.

### What it fixes:

- Long press on a file → shows context menu instead of entering selection mode

- Long press on empty area → shows empty area context menu

- Long press then drag → rubber band selection

- Short press then drag → drag file (original behavior)

### How to apply
```bash
# Clone Dolphin source
git clone https://invent.kde.org/system/dolphin.git
cd dolphin
# Download the patch:
wget https://raw.githubusercontent.com/JPTV-21/Touphinx/main/touphinx.patch
# Apply
git apply touphinx.patch
# Build
mkdir build && cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/usr
make -j$(nproc)
sudo make install
```

### For Arch Linux users
```bash
git clone https://github.com/JPTV-21/Touphinx.git
cd Touphinx
makepkg -si
```

### License
Same as Dolphin, GPL-2.0-or-later
