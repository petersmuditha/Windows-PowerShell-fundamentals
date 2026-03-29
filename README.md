# Windows-PowerShell-fundamentals

# 🖥️ Windows Command Line Mastery: Security & Administration
This repository is a comprehensive documentation and reference guide based on the Windows Command Line curriculum from TryHackMe. It focuses on leveraging the Command Prompt (CMD) for system navigation, configuration, and security auditing.

# 📝 Project Description
This repository serves as a centralized technical framework dedicated to the mastery and implementation of Windows PowerShell core concepts. It is designed as a structured repository for developing, testing, and documenting automated solutions for enterprise-level system administration.
The primary objective of this project is to bridge the gap between manual operations and automated workflows, focusing on high-level efficiency, consistency, and reliability within Windows environments.

# 🔍 What is it?
PowerShell is an advanced, cross-platform task automation solution and configuration management framework developed by Microsoft. It integrates a high-level command-line shell with a robust scripting language, architected on the .NET Core (and legacy .NET Framework) runtime.
Distinguishing it from traditional text-based shells, PowerShell is fundamentally object-oriented. This architectural choice allows for the seamless manipulation of structured data and direct interaction with system components and APIs, rather than relying on complex string parsing.

# 💼 Why is it vital to our business?
PowerShell is a cornerstone of modern operational strategy, transforming IT infrastructure from a series of manual tasks into a scalable, automated ecosystem. By implementing Infrastructure as Code (IaC) principles, it eliminates the high costs and risks associated with human error, ensuring absolute consistency across enterprise environments.
Beyond simple automation, PowerShell drives significant Return on Investment (ROI) by reallocating engineering talent from routine maintenance to high-value architectural projects. Its native integration with cloud platforms and robust auditing capabilities make it an indispensable asset for maintaining agility, security, and regulatory compliance in a competitive global market.

# 🛡️ How do we keep the system secure?
Securing a PowerShell environment relies on the principle of Least Privilege and robust execution policies. We maintain system integrity by enforcing RemoteSigned or AllSigned policies to prevent the execution of untrusted scripts and by utilizing Just-Enough-Administration (JEA) to limit user capabilities to specific tasks.
Beyond access control, security is reinforced through comprehensive Transcription and Script Block Logging, which provides a full audit trail of all activities to detect and mitigate potential exploits in real-time. By integrating sensitive credential management via SecretStore or encrypted vaults, we ensure that automation never compromises administrative credentials or environmental security.

## ⌨️ Essential Interaction: Basic Commands

Once we understand the importance of the windows command oline , the next step is learning how to communicate with the system via the Command Line Interface (CLI). Below are two fundamental commands for any security professional.

### 1. `Get-Item` 
Retrieves the specific object at the specified path (e.g., a file, a folder, or a registry key).
* **Why it matters:** Essential for inspecting the attributes of a specific target, such as its creation time, size, or permissions, without listing its contents.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 2. `Get-ChildItem` 
Lists the items (files and subdirectories) within a specified location.
* **Why it matters:** It is the primary tool for file system auditing and discovery. It allows administrators to programmatically scan directories for specific file types or outdated logs.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 3. `Set-Location` 
Sets the current working location to a specified path.
* **Why it matters:** Crucial for script navigation. It ensures that subsequent relative-path commands are executed in the correct context, preventing accidental file operations in the wrong directory.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 4. `New-Item` 
Creates a new item, such as a file, directory, or symbolic link.
* **Why it matters:** Enables automated environment provisioning. It allows scripts to build necessary folder structures or configuration files on the fly during deployment.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 5. `Remove-Item` 
Deletes the specified items.
* **Why it matters:** Vital for system hygiene and automated cleanup. It is used to purge temporary files, old logs, or decommissioned configurations to save disk space and maintain security.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 6. `Copy-Item` 
Copies an item from one location to another.
* **Why it matters:** Core for distribution and backup. It allows for the automated movement of configuration templates or the creation of redundant copies of critical data.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 7. `Get-FileHash` 
Computes the hash value (e.g., SHA256) for a file using a specified algorithm..
* **Why it matters:** Integrity verification. It ensures that a file has not been corrupted during transfer or tampered with by malicious actors.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 8. `Sort-Object` 
Sorts objects in ascending or descending order based on specific properties.
* **Why it matters:** Improves data readability and prioritization. For example, sorting processes by memory usage allows an admin to immediately identify resource-heavy applications.
  
  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 9. `Where-Object` 
Filters objects from the pipeline based on a script block or comparison operator.
* **Why it matters:** It allows you to isolate specific data points (e.g., "only services that are currently stopped") from a massive stream of information.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 10. `Select-Object` 
Selects specific properties of an object or a set of objects.
* **Why it matters:** Optimizes performance and output. By discarding unnecessary data, you reduce the memory footprint of your scripts and focus only on the relevant metrics.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 11. `Select-String` 
Finds text patterns in strings and files using regular expressions (Regex).
 **Why it matters:** Indispensable for log analysis. It allows you to search through thousands of lines of code or logs to find specific error codes or security events.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 12. `Get-ComputerInfo` 
Retrieves a consolidated list of system and operating system properties.
 **Why it matters:** Provides a comprehensive hardware and software "snapshot," which is essential for asset management and troubleshooting system compatibility.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 13. `Get-LocalUser` 
Gets the local user accounts on the computer.
 **Why it matters:** It allows admins to monitor for unauthorized accounts and verify that password policies are being applied to local users.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 14. `Get-NetIPConfiguration` 
Gets IP network configuration, including DNS and default gateway.
 **Why it matters:** Offers a high-level view of network health, making it the first step in diagnosing connectivity issues.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 15. `Get-NetIPAddress` 
Retrieves the IP addresses assigned to the network interfaces.
 **Why it matters:** Essential for low-level network troubleshooting and verifying that the correct IP/Subnet is bound to the physical or virtual adapter.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 16. `Get-NetTCPConnection` 
Displays active TCP connections and their associated ports/processes.
 **Why it matters:** It helps identify "who is talking to whom," allowing you to spot suspicious outgoing connections or unauthorized listening ports.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 17. `Get-Process` 
Gets the processes that are running on the computer.
 **Why it matters:** Fundamental for performance monitoring and management. It allows you to identify "zombie" processes or those consuming excessive CPU/RAM.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 18. `Get-Service` 
Gets the status of the services on the computer.
 **Why it matters:** Critical for ensuring system uptime. It allows for automated checks to see if essential services (like a Web Server or Database) are running and healthy.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ## 🏁 Conclusion & Next Steps

This initial documentation covers the fundamental tools required to interact with a Linux system effectively. From basic navigation  to advanced, these commands form the foundation of any **Security Operations Center (SOC)** analyst or **Penetration Tester's** daily workflow.

## 💡 My Philosophy on Technical Writing

> *"I write for clarity and structure. I'm interested in how writing can influence behavior, simplify the complex, and shift how people understand security."*  
> — inspired by [ananichoumchoum](https://github.com/ananichoumchoum)
