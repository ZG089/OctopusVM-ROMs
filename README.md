# **OctopusVM ROMs**

This repository automates the process of **downloading**, **extracting**, and **uploading** various ROMs OctopusVM as GitHub releases. It utilizes **Google Drive** as the source for the ROMs and leverages **GitHub Actions** to streamline the entire workflow.

---

## 📜 **Overview**

The GitHub Action defined in this repository performs the following tasks:

1. **Dependency Installation**: Installs the required tools, including `python3`, `gdown`, `p7zip`, and others.
2. **ROM Download**: Fetches the ROM files from Google Drive using `gdown`.
3. **File Extraction**: Unzips or extracts the downloaded ROMs into the appropriate formats (e.g., `.vmdk`, `.vhd`).
4. **Release Creation**: Automatically uploads the ROMs as assets to a **GitHub Release**.

Each workflow run creates a **new release** with a **unique tag**, based on the workflow run ID.

---

## 💾 **Included ROMs**

The following ROMs are downloaded, processed, and made available as part of the release:

- **Windows 7 Lite (x64)**
- **Windows 8.1 Ultra Lite**
- **Windows 8 Lite (No OOBE)**
- **Windows 10 Thin**
- **Windows XP Game Edition**
- **Windows 2000**
- **Windows 7 Super Lite (x86)**

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
