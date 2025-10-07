# Discord Rich Presence for Xcode (No-Idle Fork)

> **Note:** This is a modified fork of the original [xcode-discord-rpc by izyuumi](https://github.com/izyuumi/xcode-discord-rpc). The key change in this version is the complete removal of the idle-status feature.

A simple Discord Rich Presence client for Xcode. Your status will remain active as long as a project is open.

<p align="center">
  <img src="readme.png" width="400" style="max-width: 100%; height: auto;" />
</p>

## Features

- Launched in the background at login
- No menu bar icon nor dock icon
- **Presence is active as long as Xcode is running with a project open (No idle status)**
- Shows respective logos when editing [known files](#supported-file-types) and Xcode icon otherwise
- Written 100% in Rust

## Getting Started

### Installation from Source

Since this is a custom version, it needs to be built from the source code.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR-USERNAME/xcode-discord-rpc.git](https://github.com/YOUR-USERNAME/xcode-discord-rpc.git)
    cd xcode-discord-rpc
    ```

2.  **Build the project:**
    ```bash
    cargo build --release
    ```

3.  **Install the executable:**
    ```bash
    sudo cp target/release/xcode-discord-rpc /usr/local/bin/
    ```

4.  **Grant permissions:** You must manually grant Automation permissions for the application to control Xcode.
    - Go to **System Settings** > **Privacy & Security** > **Automation**.
    - Click `+`, navigate to `/usr/local/bin/`, and add `xcode-discord-rpc`.
    - Ensure the checkbox for **Xcode** is enabled.

5.  **Run the application:**
    ```bash
    xcode-discord-rpc
    ```

### Uninstallation

```bash
sudo rm /usr/local/bin/xcode-discord-rpc
