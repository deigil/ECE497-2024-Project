# 🛡️ Portable pfSense Network Security System

## Project Overview

We aim to develop a flexible, portable network security system using pfSense on a Raspberry Pi 5. This system will provide robust firewall and routing capabilities, with the added benefit of being easily reproducible across different hardware platforms using NixOS-inspired configuration management.

### Objectives

- **Portability:** Create a system that can be easily deployed on various hardware platforms, primarily targeting Raspberry Pi 5 but adaptable to other systems.
- **Reproducibility:** Implement a NixOS-like approach for system configuration, allowing easy replication and deployment of the entire system setup.
- **Security:** Leverage pfSense's powerful features to provide comprehensive network security.
- **Scalability:** Design the system to be easily upgradable and expandable.

### System Components

#### Hardware

1. 🍓 **Raspberry Pi 5:** The primary target hardware for our system.
2. 🔌 **USB 3.0 to Gigabit Ethernet Adapter:** To add additional Ethernet ports to the Raspberry Pi 5.
3. 💾 **MicroSD Card (64GB or higher):** For the operating system and pfSense installation.
4. ⚡ **Power Supply:** Compatible with Raspberry Pi 5 requirements.
5. 📦 **Enclosure:** To protect the Raspberry Pi and additional adapter.

#### Software

1. ❄️ **NixOS:** As the base operating system, providing declarative and reproducible system configuration.
2. 🛡️ **pfSense:** The core network security and routing software.
3. 🐳 **Docker:** For containerization of additional services and easier portability.
4. 🎭 **Ansible:** For automated deployment and configuration management.
5. 🐙 **Git:** For version control of configuration files and NixOS modules.

### Project Workflow

#### 1. **Base System Setup**

- 💻 Install NixOS on the Raspberry Pi 5.
- ⚙️ Create a custom NixOS configuration for pfSense compatibility.

#### 2. **pfSense Integration**

- 🔧 Develop a NixOS module for pfSense installation and configuration.
- 🌐 Configure pfSense to utilize both the onboard Ethernet and USB Ethernet adapter.

#### 3. **Configuration Management**

- 📄 Create a Nix flake for the entire system configuration, including:
  - Hardware-specific settings for Raspberry Pi 5
  - pfSense configuration
  - Network interface setup
  - Any additional software or services

#### 4. **Containerization and Portability**

- 🐳 Use Docker to containerize any additional services that complement pfSense.
- 🎭 Create Ansible playbooks for automated deployment of the entire system, including:
  - NixOS installation
  - Application of the Nix flake configuration
  - Docker container deployment

#### 5. **Testing and Optimization**

- 🧪 Thoroughly test the system on Raspberry Pi 5.
- 🔄 Verify portability by deploying the same configuration on different hardware using the Nix flake and Ansible playbooks.

#### 6. **Documentation**

- Create comprehensive documentation covering:
  - Hardware setup
  - NixOS installation and configuration
  - pfSense usage and customization
  - Deployment process using Ansible
  - Customization guidelines for different hardware platforms

### Implementation Approach

1. ❄️ **NixOS Base:** Use NixOS as the foundation, leveraging its declarative configuration model.
2. ❄️ **Nix Flakes:** Implement the entire system configuration as a Nix flake, ensuring reproducibility and easy versioning.
3. 🛡️ **pfSense Integration:** Develop custom NixOS modules to seamlessly integrate pfSense into the NixOS environment.
4. 🎭 **Ansible for Deployment:** Use Ansible for automated deployment, applying the NixOS configuration and setting up additional components.
5. 🐳 **Docker for Portability:** Containerize any additional services using Docker to ensure consistency across different hardware platforms.

### Next Steps

- 🍓 Set up a Raspberry Pi 5 with NixOS and create a basic configuration.
- 🛡️ Develop a NixOS module for pfSense integration.
- ❄️ Create a Nix flake encompassing the entire system configuration.
- 🎭 Write Ansible playbooks for automated deployment.
- 🧪 Test the system on Raspberry Pi 5 and at least one other hardware platform.
- 📚 Document the entire process and create user guides.

This approach combines the power of pfSense with the flexibility and reproducibility of NixOS, wrapped in an easily deployable package using Ansible and Docker. It allows for a highly portable and customizable network security solution that can be quickly deployed on various hardware platforms while maintaining consistency in configuration and functionality.
