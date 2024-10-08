# **OctopusVM ROMs**

This repository automates the process of **downloading**, **extracting**, and **uploading** various ROMs OctopusVM as GitHub releases. It utilizes **Google Drive** as the source for the ROMs and leverages **GitHub Actions** to streamline the entire workflow.

---

## 💾 **Included ROMs**

The following ROMs are downloaded, processed, and made available as part of the release:

- **Windows 7 Lite (x64)**

- **Windows 8.1 Ultra Lite**

- **Windows 8 Lite (NoOOBE Version)**

- **Windows 10 Thin**

- **Windows XP Game Edition**

- **Windows 2000**

- **Windows 7 Super Lite (x86)**

- **Arch Linux (non GUI / old version 2017 but still working well, Maybe will release the latest version soon for OctopusVM)**

- **Kolibri Linux**

- **TinyCoreLinux Plus v14.0, (old version but still working well, Maybe will release the latest verison 15.0 soon for OctopusVM)**

- **Linux Mint 10**

- **Lubuntu 18.04 (old version 2018 but still working well, Maybe will release the latest version soon for OctopusVM)**

- **AlpineLinux x86 Xfce4**

- **RedHat Linux**

- **Rubuntu v10.04 Lite x86**

- **TinyCore v12.0 (old version 2018 but still working well, Maybe will release the latest version soon for OctopusVM)**

- **Note: If you downloaded any zip file don't unzip it let OctopusVM unzip it, and let all the ROMs in the Download Folder, If you downloaded it via 1DM, ADM, or any other Download Manager move it to Download Folder.**
---

## ⚙️ **How It Works**

This repository includes a **GitHub Actions** workflow that automates the complete ROM release process. Below is a detailed breakdown:

1. **Triggering the Workflow**:
   - The workflow can be triggered manually via the **GitHub UI** using the `workflow_dispatch` event.
   
2. **Installing Required Packages**:
   - Necessary packages such as `gdown`, `7zip`, and `unzip` are installed to handle file downloads and extraction.

3. **Downloading and Extracting ROM Files**:
   - ROMs are downloaded from specified Google Drive URLs using `gdown`.
   - The downloaded files are then extracted using **7z** or **unzip**, based on their format.

4. **Uploading to GitHub Releases**:
   - After processing, the ROM files are uploaded as assets to a **new GitHub release** using the `softprops/action-gh-release` action.

---

## 🚀 **Usage**

### **Manually Triggering the Workflow**

You can manually trigger the workflow to process and release the ROMs:

1. Go to the **Actions** tab in your repository.
2. Select the workflow named **"Release OctopusVM ROMs"**.
3. Click on **"Run workflow"** to initiate the process.
