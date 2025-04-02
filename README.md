# Microsoft Office Activation Guide

This repository provides guidance for activating Microsoft Office on different operating systems.

## Windows 10/11 Activation

You can activate Office on Windows without using cracks by using the Mass Activation Script.

### Quick Steps:

1. Right-click on the Windows start menu and select PowerShell or Terminal (not CMD)
2. Copy-paste the following code and press Enter:
   ```PowerShell
   irm https://massgrave.dev/ias | iex
   ```
3. Follow the on-screen instructions in the activation menu
4. Activation complete!

## macOS Activation Methods

### For Office 2019 and Above

Office 2019 and newer versions require using the Volume License (VL) Serializer tool:

1. Install Office 2019 for macOS:
   - Download from [Microsoft macadmins.software](https://macadmins.software/)
   - Or use the [Official Microsoft Installer](https://go.microsoft.com/fwlink/?linkid=525133)
   - Alternatively, install via Homebrew: `brew install --cask microsoft-office`

2. **Important**: Do not launch any Office applications after installation

3. Download and install the VL Serializer:
   - [Microsoft Office 2019 VL Serializer](https://gist.github.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a/raw/Microsoft_Office_2019_VL_Serializer.pkg)

4. Run the VL Serializer to automatically activate Office 2019

5. Launch your Office applications

#### Troubleshooting

If you're still prompted to sign in after activation:
- Try using the [Microsoft Office License Removal Tool](https://go.microsoft.com/fwlink/?linkid=849815)
- Then reinstall Office and run the Serializer again

### For Office 2016 (Legacy Method)

Office 2016 can be activated using a license file:

1. Install Office 2016 for macOS:
   - Download from [Microsoft macadmins.software](https://macadmins.software/)
   - Or use the [Official Link for Office 2016 Volume License](https://go.microsoft.com/fwlink/?linkid=871743)

2. **Important**: Do not launch any Office applications after installation

3. Copy the license file to the Preferences folder:
   ```bash
   curl -sSL https://gist.githubusercontent.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a/raw/com.microsoft.office.licensingV2.plist -o /Library/Preferences/com.microsoft.office.licensingV2.plist
   ```

4. Launch your Office applications

## References

- [Overview of the Volume License Serializer](https://docs.microsoft.com/en-us/deployoffice/mac/volume-license-serializer)
- [Volume License Serializer (简体中文)](https://docs.microsoft.com/zh-cn/deployoffice/mac/volume-license-serializer)
- [Microsoft Office for Mac Admin Resources](https://macadmins.software/)

## Note

This guide is provided for educational purposes. Always ensure you have the proper licenses for software you use in commercial environments.
