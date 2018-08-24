# Microsoft Intune Win32 App Packaging Tool
Manage Windows Apps (.intunewin) with Intune

[Version 1.2](https://github.com/Microsoft/Intune-Win32-App-Packaging-Tool/releases/tag/Version_1.2)

[See release notes for more information.](https://github.com/Microsoft/Intune-Win32App-Wrapping-Tool/releases)

Use the Microsoft Intune Win32 App Packaging Tool to pre-process Windows Classic apps. The packaging tool converts application installation files into the .intunewin format. The packaging tool also detects the parameters required by Intune to determine the application installation state. After you use this tool on your apps, you will be able to upload and assign the apps in the Microsoft Intune console.

Before you install and the use Microsoft Intune Win32 App Packaging Tool you **must**:
* Review the [Microsoft License Terms for Microsoft Intune Win32 App Packaging Tool](https://github.com/Microsoft/Intune-Win32App-Wrapping-Tool/blob/master/Microsoft%20License%20Terms%20For%20Win32%20App%20Packaging%20Tool.pdf). Print and retain a copy of the license terms for your records. By downloading and using Microsoft Intune Win32 App Packaging Tool, you agree to such license terms. If you do not accept them, do not use the software.
* Review the [Microsoft Intune Privacy Statement](https://docs.microsoft.com/legal/intune/microsoft-intune-privacy-statement) for information on the privacy policy of the Intune Win32 App Packaging Tool.

Sample commands to use for the Microsoft Intune Win32 App Packaging Tool:
* IntuneWinAppUtil -h
  * This will show usage information for the tool.
* IntuneWinAppUtil -c <setup_folder> -s <source_setup_file> -o <output_folder> <-q>
  * This will generate the .intunewin file from the specified source folder and setup file.
  * For MSI setup file, this tool will retrieve required information for Intune.
  * If -q is specified, it will be in quiet mode. If the output file already exists, it will be overwritten.
  * Also if the output folder does not exist, it will be created automatically.
* IntuneWinAppUtil
  * If no parameter is specified, this tool will guide you to input the required parameters step by step.

Command-line parameters available
* -h  Help
* -c  <setup_folder>   Setup folder for all setup files.
* -s  <setup_file>     Setup file (e.g. setup.exe or setup.msi).
* -o  <output_file>    Output folder for the generated .intunewin file.
