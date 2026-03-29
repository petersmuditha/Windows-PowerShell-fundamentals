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

### 10. `netstat` 
Displays all active network connections (incoming and outgoing) and listening ports.
* **Why it matters:** Provides Visibility. It helps admins see if a computer is communicating with an unauthorized external server.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 11. `netstat -abon` 
A powerful variation that shows the executable (program) involved in every connection, along with the Process ID (PID).
 **Why it matters:** A key Cybersecurity tool. If a computer is infected with malware, netstat -abon can reveal exactly which "hidden" program is sending data to a hacker's server.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 12. `dir` 
Lists the files and subdirectories in the current directory.
 **Why it matters:** Provides immediate visibility into what is stored on a drive.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 13. `dir /a` 
Lists all files, including those with hidden or system attributes.
 **Why it matters:** Critical for Security and Troubleshooting. Malware often hides its files by setting the "hidden" attribute; this command ensures nothing stays out of sight.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 14. `dir /s` 
Displays files in the current directory and all subdirectories.
 **Why it matters:** A powerful Search Tool. It allows an admin to find a specific lost file across an entire hard drive from a single command.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 15. `tree` 
Graphically displays the folder structure of a drive or path.
 **Why it matters:** Excellent for Documentation. It helps IT managers visualize complex folder hierarchies when organizing shared company drives or project structures.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 16. `mkdir` 
Creates a new folder.
 **Why it matters:** Used in Deployment Scripts to automatically create necessary folders for new software or user profiles.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 17. `rmdir` 
Deletes a folder.
 **Why it matters:** Used for System Cleanup to remove old, obsolete project folders and reclaim disk space.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 18. `copy` 
Copies one or more files to another location.
 **Why it matters:** Fundamental for Data Backups. It allows for the quick duplication of critical configuration files before making changes.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 19. `move` 
Moves files or renames directories.
 **Why it matters:** Essential for Data Migration. It allows for the reorganization of files without creating unnecessary duplicates.
  
  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 20. `erase` 
Deletes one or more files.
 **Why it matters:** Vital for Privacy and Maintenance. It is used to wipe temporary files or sensitive data that is no longer needed by the organization.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 21. `tasklist` 
Displays a list of all currently running processes (apps and services) along with their memory usage.
 **Why it matters:** A key Performance and Security Audit tool. If a computer is slow, tasklist identifies the "resource hog." If a computer is suspected of having a virus, it allows the admin to see if any suspicious, unrecognized programs are running in the background.
  
  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ## 🏁 Conclusion & Next Steps

This initial documentation covers the fundamental tools required to interact with a Linux system effectively. From basic navigation  to advanced, these commands form the foundation of any **Security Operations Center (SOC)** analyst or **Penetration Tester's** daily workflow.

## 💡 My Philosophy on Technical Writing

> *"I write for clarity and structure. I'm interested in how writing can influence behavior, simplify the complex, and shift how people understand security."*  
> — inspired by [ananichoumchoum](https://github.com/ananichoumchoum)
