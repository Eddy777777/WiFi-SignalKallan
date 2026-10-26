WIFI SIGNAL KALLAN BY EDDY77

## 🔍 Overview

WiFiSignal kallan is a powerful, pure Python implementation of a WiFi deauthentication tool that doesn't rely on the Aircrack-ng suite. It provides an automated, user-friendly approach to WiFi analysis and deauthentication testing.

**Key Features:**
-  Automatic network interface detection
-  Access point scanning with detailed information
-  Client device discovery
-  Targeted and broadcast deauthentication
-  Signal strength monitoring
-  Clean, colorful command-line interface

## ⚡ Advantages Over Aircrack-ng

WiFi signal kallan offers several benefits compared to traditional Aircrack-ng based tools:

- **Pure Python Implementation**: No dependency on external C-based tools or libraries
- **Simplified Workflow**: Single command operation vs multi-step process in Aircrack-ng
- **Automatic Interface Management**: Auto-detection and mode switching without manual steps
- **Lower Footprint**: Lighter resource usage compared to full Aircrack-ng suite
- **Modern Codebase**: Python-based for easier customization and extension
- **Single Tool**: All functionality in one command vs multiple tools (airmon-ng, airodump-ng, aireplay-ng)

## ⚠️ Disclaimer

**This tool is provided for EDUCATIONAL PURPOSES ONLY.**

WiFi signal kallan  is designed for network administrators and security professionals to test their own networks. Using this tool on networks without explicit permission is illegal in most jurisdictions and unethical. The author accepts NO responsibility for misuse of this tool.

## 🔧 Requirements

- Linux-based operating system
- Python 3.x
- WiFi adapter supporting monitor mode and packet injection
- Root privileges

## 🔌 Supported Network Adapters

WiFi signal kallan  works with most WiFi adapters that support monitor mode ( Most modern laptops has inbuild monitor mode supporting wifi adapters ), including:
- Alfa AWUS036ACH
- TP-Link TL-WN722N (v1)
- Many other Atheros, Ralink, and Realtek chipset-based adapters



## 🚀 Usage

### Basic Usage
```bash
sudo wifi signal kallan
```
This will auto-detect your network interfaces and guide you through the attack options.

### Specifying Network Interface
```bash
sudo wifi Signal kallan -i [interface_name]
# Example
sudo wifi Signal kallan -i wlan0
```

### Advanced Options

#### Target Specific Devices
```bash
# Set gateway (access point) MAC address manually
sudo wifi signal kallan -g [gateway_mac]

# Set target client MAC address manually
sudo wifi signal kallan -t [target_mac]

# Deauthenticate all clients
sudo wifi signal kallan  -t 0
```

#### Combined Parameters
```bash
sudo wifi -i [interface] -g [gateway_mac] -t [target_mac]
# Example:
sudo wifi signal kallan -i wlan0 -g 11:22:33:44:55:66 -t aa:bb:cc:dd:ee:ff
```

#### Interface Management
```bash
# Set interface to managed mode
sudo wifi signal kallan --man [interface]

# Set interface to monitor mode
sudo wifi signal kallan --mon [interface]
```

| Command | Description |
|---------|-------------|
| `-i`, `--interface` | Specify network interface |
| `-g`, `--gateway_mac` | Set access point MAC address |
| `-t`, `--target_mac` | Set target client MAC address |
| `-l`, `--list_interface` | List available network interfaces |
| `-sw`, `--scan_wifi` | Scan for WiFi networks |
| `-st`, `--scan_target` | Scan for connected clients |
| `--man` | Set interface to managed mode |
| `--mon` | Set interface to monitor mode |
