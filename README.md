# Local Manifest for Poco X6 Pro 5G / Redmi K70E

This repository contains the manifest for building a custom ROM for the Poco X6 Pro 5G / Redmi K70E.

# How To Use:
1. After doing a `repo init -u <manifest-url>`, create a directory for your local manifests:

   ```bash
   cd .repo
   mkdir local_manifests
   cd local_manifests

2. Create a new file for your local manifest:
nano local_manifests.xml

3. Then paste the following XML configuration to specify the necessary repositories for the Poco X6 Pro 5G / Redmi K70E: (THIS IS A EXAMPLE ONLY NOT ROMS ARE USING THE SAME!!!)

<?xml version="1.0" encoding="UTF-8"?>
<manifest>
    <remote name="Quantum-Orbit" fetch="https://github.com/Quantum-Orbit" />
    <remote name="Quantum-Orbit-gitea" fetch="https://gitea.com/Quantum-Orbit" />

    <default revision="master" remote="Quantum-Orbit" sync-j="4" />

    <project name="device/xiaomi/duchamp" path="device/xiaomi/duchamp" />
    <project name="device/xiaomi/duchamp-kernel" path="device/xiaomi/duchamp-kernel" />
    <project name="kernel/xiaomi/mt6897" path="kernel/xiaomi/mt6897" />
    <project name="vendor/xiaomi/duchamp" path="vendor/xiaomi/duchamp" />
    <project name="hardware/mediatek" path="hardware/mediatek" />
    <project name="hardware/xiaomi" path="hardware/xiaomi" />
    <project name="device/mediatek/sepolicy_vndr" path="device/mediatek/sepolicy_vndr" />
</manifest>

4. Save the file and exit the editor:

# In nano, press CTRL+O to save, then press ENTER, and CTRL+X to exit


5. Finally, sync the repositories:
repo sync

Repositories:
- `device/xiaomi/duchamp`: Device configuration
- `device/xiaomi/duchamp-kernel`: Kernel source
- `kernel/xiaomi/mt6897`: MediaTek kernel source
- `vendor/xiaomi/duchamp`: Vendor files
- `hardware/mediatek`: MediaTek hardware configs
- `hardware/xiaomi`: Xiaomi hardware configs
- `device/mediatek/sepolicy_vndr`: SELinux policies

Remote Repositories:
- GitHub: `https://github.com/Quantum-Orbit`
- Gitea: `https://gitea.com/Quantum-Orbit`

Contributing:
Feel free to fork and submit pull requests.
