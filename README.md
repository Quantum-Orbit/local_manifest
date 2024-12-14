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
   <remote name="QuantumOrbit"
	    fetch="https://github.com/Quantum-Orbit"
	    clone-depth="1" />
   <remote name="Quantum-Orbit"
	    fetch="https://gitea.com/Quantum-Orbit"
	    clone-depth="1" />

<!--Tree -->
<project path="device/xiaomi/duchamp" name="device_xiaomi_duchamp" remote="QuantumOrbit" revision="udc" />

<!--Kernel -->
<project path="device/xiaomi/duchamp-kernel" name="device_xiaomi_duchamp-kernel" remote="QuantumOrbit" revision="lineage-21" />
<project path="kernel/xiaomi/mt6897" name="kernel_xiaomi_mt6897" remote="QuantumOrbit" revision="lineage-21" />

<!--Vendor -->
<project path="vendor/xiaomi/duchamp" name="android_vendor_xiaomi_duchamp" remote="Quantum-Orbit" revision="lineage-21" />

<!--stuff -->
<project path="hardware/mediatek" name="hardware_mediatek" remote="QuantumOrbit" revision="lineage-21" />
<project path="hardware/xiaomi" name="hardware_xiaomi" remote="QuantumOrbit" revision="lineage-21" />
<project path="device/mediatek/sepolicy_vndr" name="device_mediatek_sepolicy_vndr" remote="QuantumOrbit" revision="fifteen"/>
</manifest>

4. Save the file and exit the editor:

# In nano, press CTRL+O to save, then press ENTER, and CTRL+X to exit


5. Finally, sync the repositories:
repo sync (depends what command are using on other roms)

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
