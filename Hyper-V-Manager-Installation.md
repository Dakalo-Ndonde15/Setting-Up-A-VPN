# <a href="https://youtu.be/1fCIJDqz9rY/">Hyper-V Manager Setup Guide</a>


## Description
This project serves as a comprehensive guide to installing and enabling Hyper-V Manager on Windows systems. Hyper-V is a built-in Windows feature that allows users to create and manage virtual machines. This step-by-step guide walks through the process of verifying system prerequisites, enabling the necessary features, and configuring Hyper-V Manager for use. The project is ideal for users who want to set up a virtualization environment for testing, development, or training purposes.

## Languages and Utilities Used
- **Windows Features**
- **Command Prompt**
- **Hyper-V Manager**

## Environments Used
- **Windows 11 Pro/Enterprise** (22H2)

## Prerequisites
- Ensure that virtualization is enabled in your system BIOS/UEFI settings.
- Verify that your system meets the hardware requirements for Hyper-V.
- Use Windows Pro or Enterprise editions, as Hyper-V is not available on Home editions.

## Walk-through Steps

### Open Windows Features:
- Click the magnifying glass icon in the taskbar, search for "Windows Features," and open it from the search results.

<p align="center">
  <img src="https://imgur.com/ArTL6YF.png" height="80%" width="80%" alt="Search Windows Features" />
  <br/>
  <img src="https://imgur.com/Q761NMR.png" height="80%" width="80%" alt="Open Windows Features" />
</p>

### Enable Hyper-V:
- In the Windows Features window, find "Hyper-V," check the box next to it, and click "OK" to apply the settings.

<p align="center">
  <img src="https://imgur.com/DbPaAhy.png" height="80%" width="80%" alt="Enable Hyper-V" />
</p>

### Restart the Computer:
- After applying the settings, restart your computer.

<p align="center">
  <img src="https://imgur.com/e3cBk5u.png" height="80%" width="80%" alt="Restart Windows" />
</p>

### Access Hyper-V Manager:
- After restarting, click the magnifying glass icon, search for "Hyper-V," and open it.
- Alternatively, open Command Prompt and type `systeminfo` to verify if Hyper-V is installed.

<p align="center">
  <img src="https://imgur.com/wWeo33K.png" height="80%" width="80%" alt="Open Hyper-V Manager" />
  <br/>
  <img src="https://imgur.com/gaFj3PE.png" height="80%" width="80%" alt="Open Hyper-V Manager" />
</p>

### Create a Test Virtual Machine:
- Open Hyper-V, connect your local machine, right-click on the local machine, select **New**, and click **Virtual Machine**.
- Follow the setup wizard to create a virtual machine.

<p align="center">
  <img src="https://imgur.com/hHNS7o9.png" height="80%" width="80%" alt="Create Virtual Machine" />
  <br/>
  <img src="https://imgur.com/JLxBtnI.png" height="80%" width="80%" alt="Create Virtual Machine next 1" />
  <br/>
  <img src="https://imgur.com/VKnG0ld.png" height="80%" width="80%" alt="Create Virtual Machine next 2" />
  <br/>
  <img src="https://imgur.com/WLcAter.png" height="80%" width="80%" alt="Create Virtual Machine next 3" />
  <br/>
  <img src="https://imgur.com/bQi4nmC.png" height="80%" width="80%" alt="Create Virtual Machine next 4" />
  <br/>
  <img src="https://imgur.com/o9bGazx.png" height="80%" width="80%" alt="Create Virtual Machine next 5" />
  <br/>
  <img src="https://imgur.com/xN3cIFk.png" height="80%" width="80%" alt="Create Virtual Machine next 6" />
  <br/>
  <img src="https://imgur.com/rPxnhGK.png" height="80%" width="80%" alt="Create Virtual Machine next 7" />
  <br/>
  <img src="https://imgur.com/ONrRe4Q.png" height="80%" width="80%" alt="Create Virtual Machine finish 8" />
  <br/>
  <img src="https://imgur.com/kA3wJna.png" height="80%" width="80%" alt="Test machine created 9" />
  <br/>
</p>

### Opening your virtural Machine

<p align="center">Right-click the test virtual machine and click Start.</p>
<p align="center">
  <img src="https://imgur.com/SBoIAjZ.png" height="80%" width="80%" alt="Test machine open 10" />
</p>

<p align="center">If you encounter an error, it may look like this:</p>
<p align="center">
  <img src="https://imgur.com/JYwgM28.png" height="80%" width="80%" alt="Test machine open failed 11" />
</p> 

**Note:** This is because we have not yet added or installed an operating system (OS) to the virtual machine. Hence, the virtual machine will not function until an operating system (OS) is added and installed. Ensure you have the OS installation media (e.g., ISO file) ready to complete the setup.

Here is a helpful video on adding OS to the virtual machine: [Full Guide - Setting up a Virtual Machine](https://www.youtube.com/watch?v=g_eaMpxoCWo)

## Conclusion
- You have now successfully installed Hyper-V and created a virtual machine.
