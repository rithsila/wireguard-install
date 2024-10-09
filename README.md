WireGuard Installation Script
This script automates the installation and management of a WireGuard VPN server on Linux systems. It provides an easy-to-use interface for setting up WireGuard, managing clients, and handling server configurations.
Features

Automated WireGuard server installation
Easy client management (add, list, revoke)
Support for multiple Linux distributions
Automatic firewall configuration
QR code generation for client configs
IPv4 and IPv6 support

Requirements

A supported Linux distribution:

Ubuntu 18.04+
Debian 10+
Fedora 32+
CentOS 8+
AlmaLinux 8+
Rocky Linux 8+
Oracle Linux 8+
Arch Linux


Root access
A public IP address (IPv4 or IPv6)
```markdown
# WireGuard Installer

This script automates the installation and management of WireGuard VPN on various Linux distributions, including support for both OpenVZ and KVM environments. It also allows for the adjustment of the MTU (Maximum Transmission Unit) to optimize network performance.

## Features

- **Automated Installation**: Easily install WireGuard on Debian, Ubuntu, Fedora, CentOS, AlmaLinux, Rocky Linux, Oracle Linux, and Arch Linux.
- **Environment Support**: Supports both OpenVZ and KVM environments.
- **MTU Adjustment**: Allows users to specify the MTU during installation to optimize network performance.
- **Client Management**: Add, list, and revoke clients.
- **Uninstallation**: Easily uninstall WireGuard and remove all configuration files.

## Prerequisites

- A server running one of the supported Linux distributions.
- Root access to the server.

## Installation

1. **Download the Script**:
   ```bash
   wget https://raw.githubusercontent.com/yourusername/wireguard-install/main/wireguard-install.sh
   ```

2. **Make the Script Executable**:
   ```bash
   chmod +x wireguard-install.sh
   ```

3. **Run the Script with Root Privileges**:
   ```bash
   sudo ./wireguard-install.sh
   ```

## Usage

### Initial Installation

When you run the script for the first time, it will guide you through the installation process. You will be prompted to provide the following information:

- **Public IP Address**: The public IP address of your server.
- **Public Interface**: The network interface connected to the internet.
- **WireGuard Interface Name**: The name of the WireGuard interface (default is `wg0`).
- **Server WireGuard IPv4**: The IPv4 address for the WireGuard server.
- **Server WireGuard IPv6**: The IPv6 address for the WireGuard server.
- **Server Port**: The port on which WireGuard will listen.
- **Client DNS**: The DNS resolvers to use for clients.
- **Allowed IPs**: The IP ranges that clients can access through the VPN.
- **MTU**: The Maximum Transmission Unit (MTU) for the WireGuard interface.

### Managing Clients

After the initial installation, you can manage clients using the following options:

1. **Add a New Client**:
   - Run the script and select option `1` to add a new client.
   - Follow the prompts to configure the new client.

2. **List All Clients**:
   - Run the script and select option `2` to list all existing clients.

3. **Revoke an Existing Client**:
   - Run the script and select option `3` to revoke an existing client.
   - Select the client to revoke from the list.

### Uninstallation

To uninstall WireGuard and remove all configuration files:

1. Run the script and select option `4`.
2. Confirm the uninstallation when prompted.

## Troubleshooting

- **WireGuard Not Running**: If WireGuard does not start after installation, check the status with `systemctl status wg-quick@wg0`. If you see an error like "Cannot find device wg0", try rebooting the server.
- **No Internet Connectivity**: If clients cannot access the internet, ensure that the server's firewall rules are correctly configured and that the server has internet connectivity.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- This script is based on the work of [Nyr](https://github.com/Nyr/wireguard-install) and [angristan](https://github.com/angristan/wireguard-install).
- Special thanks to the WireGuard community for their continuous support and development.

---

For any questions or issues, please open an issue on GitHub.
```

### Key Sections:
1. **Features**: Highlights the main features of the script.
2. **Prerequisites**: Lists the requirements for running the script.
3. **Installation**: Provides step-by-step instructions for downloading, making the script executable, and running it.
4. **Usage**: Describes how to use the script for initial installation, managing clients, and uninstalling WireGuard.
5. **Troubleshooting**: Offers common troubleshooting tips.
6. **Contributing**: Encourages contributions and provides guidelines.
7. **License**: Specifies the license under which the project is distributed.
8. **Acknowledgments**: Gives credit to the original authors and the WireGuard community.

Save this content to a file named `README.md` in the root of your GitHub repository. This will provide users with clear instructions and information about your WireGuard installation script.
