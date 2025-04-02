# Crack-Microsoft-MacOS

> [!NOTE]  
> ## For every body who using **Win10/11** with new Office that you need to know:
>
> to active Office without crack, just follow https://github.com/WindowsAddict/IDM-Activation-Script, 
> 
> you wiil only need to run 
> 
> ```PowerShell
> irm https://massgrave.dev/ias | iex
> ```
> in PowerShell

Step By Step:
> - Right-click on the Windows start menu and select PowerShell or Terminal (Not CMD).
> - Copy-paste the below code and press enter
> - `irm https://massgrave.dev/ias | iex`
> - You will see the activation options, follow the on-screen instructions.
> - That's all.


<br/>

---

> **The Legacy Archived Content:**
>
> Note: This method will not keep update for macOS


# [Archived] Activate MS Office 2019/2016 for macOS - Microsoft_Office_2019_VL_Serializer

## Office 2019 above

2019-06-03

Note that Office2019 **DO NOT** support activate via simple copy/paste plist license file which is the simplest way to activate Office 2016.
Fortunately, you can also use the **VL Serializer** tool, just install Office 2019 and Serializer, then run Serializer to activate.

### Ref

- [Overview of the Volume License (VL) Serializer](https://docs.microsoft.com/en-us/deployoffice/mac/volume-license-serializer)
- [Overview of the Volume License (VL) Serializer (简体中文)](https://docs.microsoft.com/zh-cn/deployoffice/mac/volume-license-serializer)



### Activation Step

1. **DO NOT RUN OFFICE APP AFTER INSTALLED**, but just install Office 2019 for macOS, choose one of this

   - manual download ref: https://macadmins.software/
   - [Official Link - Microsoft_Office_16.27.19071500_Installer.pkg](https://officecdn.microsoft.com/pr/C1297A47-86C4-4C1F-97FA-950631F94777/MacAutoupdate/Microsoft_Office_16.27.19071500_Installer.pkg)
   - [Official Link - Office 2019 Volume License 16.x latest](https://go.microsoft.com/fwlink/?linkid=525133)

   or install via brew:

   ```bash
   brew cask install microsoft-office
   ```

2. manual download and install [**Microsoft_Office_2019_VL_Serializer.pkg**](https://gist.github.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a#file-microsoft_office_2019_vl_serializer-pkg)

   - [`Microsoft_Office_2019_VL_Serializer.pkg` in this gist](https://gist.github.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a/raw/Microsoft_Office_2019_VL_Serializer.pkg) (have tested to work with v16.27, but not work with >= v16.80)
   - [`Microsoft_Office_2019_VL_Serializer.pkg` official link]( https://www.microsoft.com/licensing/servicecenter)

3. run `Microsoft_Office_2019_VL_Serializer` and it will automatic activate Office 2019

4. open the office app, completed.


### Note

If you alaways been asked for 'Sign in' and still requires activation, please try to [remove Office license files on a Mac](https://support.office.com/en-us/article/how-to-remove-office-license-files-on-a-mac-b032c0f6-a431-4dad-83a9-6b727c03b193).
[Here](https://go.microsoft.com/fwlink/?linkid=849815) is the official download link for [Microsoft_Office_License_Removal](https://go.microsoft.com/fwlink/?linkid=849815) tool. (thanks for @lidroider's [comment](https://gist.github.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a?permalink_comment_id=3070164#gistcomment-3070164))

The [`Serializer.pkg` in this gist](https://gist.github.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a/raw/Microsoft_Office_2019_VL_Serializer.pkg) is signature by Microsoft Corporation Official.
To check it, you can see details [in this comment](https://gist.github.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a?permalink_comment_id=3004329#gistcomment-3004329) (2019-08-21)


## Office 2016 16.11 for macOS VL2 license

2018-04-25

### Ref

- VLSC ref: https://blog.csdn.net/cneducation/article/details/50573649
- License ref: https://bbs.feng.com/read-htm-tid-10731033.html

### Activation Step

1. install Office2016 for mac with Office Suite Install, but **DO NOT RUN OFFICE AFTER INSTALLED**
   - manual download ref: https://macadmins.software/
   - [Official Link - Office 2016 Volume License 16.16.10](https://go.microsoft.com/fwlink/?linkid=871743)

    or install via brew:

    ```bash
    # brew cask install microsoft-office  # this point to Office 2019 now
    # install last office 2016 version below
    brew cask install https://github.com/Homebrew/homebrew-cask/raw/538c7cf34c085e3bb4fdac36f6370ded87930036/Casks/microsoft-office.rb
    ```

2. copy license file `com.microsoft.office.licensingV2.plist` to `Preferences`

    ```bash
    # md5(com.microsoft.office.licensingV2.plist) = a8f1283303838b4d3bd943775e463239
    cp com.microsoft.office.licensingV2.plist /Library/Preferences/

    # or download it in library by command line
    curl -sSL https://gist.githubusercontent.com/zthxxx/9ddc171d00df98cbf8b4b0d8469ce90a/raw/com.microsoft.office.licensingV2.plist -o /Library/Preferences/com.microsoft.office.licensingV2.plist
    ```

3. run the office app, completed.
