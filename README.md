# Getting Started

> ## ⚠️ WARNING ⚠️
> 
> - **Read every step, You may miss key steps in making the EFI work.**
> - **Always back up your sensitive data before continuing. This may be a destructive process.**
> - **If you do not own more than one device (running windows or linux or macOS), please create a windows or ubuntu installer to use in case macos doesnt boot up after installation.**

## SMBIOS Confguration:

This EFI does not include the SMBIOS, to configure it we have two options:

- [Using Third Party Software (easier)](https://github.com/sxn4y/dell-latitude-7480-opencore-efi/edit/main/README.md#using-third-party-software)
- [Using GenSMBIOS (official method).](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html#platforminfo)

### Using Third Party Software:

We will be using a software called OCAT (OCAuxiliaryTools), It generates the SMBIOS and auto injects it into the config automatically. I personally use this to make all my configs, as it has a bunch of useful features such as auto syncing with my EFI folder (Kexts and Drivers) and auto imports plugins for kexts.

You can find the download [here](https://github.com/ic005k/OCAuxiliaryTools/releases)!

Thank you; [@ic005k](https://github.com/ic005k), for making this much less tedious.

Let's get started,
1. Find the config.plist file located in this directory:<img width="965" height="697" alt="image" src="https://github.com/user-attachments/assets/1ccefe40-4822-474a-ae65-39bd47b65da8" />
2. Open it using OCAuxiliaryTools.app which you should've installed before starting:<img width="634" height="338" alt="image" src="https://github.com/user-attachments/assets/092efa75-b655-4f28-85ed-0de48b4f25c1" />
3. Go to PI (PlatformInfo) and click on the Generate button for the whole SMBIOS:<img width="1164" height="766" alt="image" src="https://github.com/user-attachments/assets/30af06b4-9cec-481a-8d61-ae61323b8648" />
4. After that, your SMBIOS may be populated. but we're not done, generate the ROM as well before saving the file by pressing Ctrl/Cmd+S. <img width="1164" height="766" alt="image" src="https://github.com/user-attachments/assets/caab9397-dda8-4e1b-9603-7458a79fe565" />
5. Congrats! You've Successfully Generated your SMBIOS using OCAT. Now copy the EFI folder (no need for the readme.md file) into a usb drive formatted in fat32. For more info refer [Creating the USB](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) from the official OpenCore Install Guide.
