# StaticMicVolumeApp
Forces microphone level to a fixed user-set value. App minimizes to tray without a taskbar icon.

### Intention
I created this app as a solution for the gazillion different applications and/or games that change the levels of your microphone without asking.
Results of this are people yelling at you to turn down the volume on your mic because your levels are way too high.

### Features (v1.2.0.0)
- Frontend (Windows Forms)
- Select any Mic from ComboBox
- Set Volume in Percent
- Set Interval for checking in Seconds
- Minimize to Tray without Taskbar icon
- Start by providing command line parameters
 
### Example for starting with command line parameters
```
StaticMicVolumeApp.exe -v 30
StaticMicVolumeApp.exe --volume 30 --interval 10
StaticMicVolumeApp.exe -v 30 -i 10
StaticMicVolumeApp.exe -v 30 --name SubStringOfMyMicName
StaticMicVolumeApp.exe -v 30 -n SubStringOfMyMicName
```

### Example autorun on startup
1. Open the Registry Editor (**Win+R**, enter `regedit` and hit **OK**)
2. Navigate to Registry Key `Computer\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`
3. **Edit** > **New** > **String Value** and name it `StaticMicVolumeApp` or similar.
4. Select the new entry, then **Edit** > **Modify...**
5. In the **Value data** field enter the path to the app and the command line parameters you want to use.
```
"C:\Path\To\StaticMicVolumeApp.exe" --volume 30 --interval 10
```
![image](https://github.com/user-attachments/assets/9de7f3d5-054d-43be-9d2f-65e4fb37119d)

### Dependencies
- NAudio v1.7.3 https://www.nuget.org/packages/NAudio/1.7.3
- Command Line Parser Library v2.0.261-beta https://github.com/gsscoder/commandline
- MoreLinq v1.1.1 https://www.nuget.org/packages/morelinq/1.1.1


