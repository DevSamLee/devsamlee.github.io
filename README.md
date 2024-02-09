# devsamlee.github.io
This repo contains contents of cybersecurity and cloud computing

## Windows Hardening

### Windows Update
Windows has a schedule for making their updates available which is every Tuesday, also know as Patch Tuesday.

### Local Group Policy Console
Type in the Run command:
gpedit.msc

Expand "Computer Configuration" by clicking on the small arrow.

Expand "Administrative Templates".

Expand "Windows Components".

Expand "Microsoft Defender Antivirus".

Select "Real-Time Protection".

Click on "Turn off Real time protection".

A description of the policy will appear on the left.

Right click on "Turn off Real time protection".

Select "edit".

Select "disabled" .

Click "OK".

![image](https://github.com/DevSamLee/devsamlee.github.io/assets/96956309/689df12f-b9b6-404a-af32-ac0da8e3ebb5)


### Windows Security Setting
Click "restore firewalls to default". All settings will be set to default.

If anyone else had configured firewall rules then they would be reset to default settings.

![image](https://github.com/DevSamLee/devsamlee.github.io/assets/96956309/b3688a81-bf18-452c-b5c7-4716378bd70c)


### Remote Desktop Setting
Type “remote settings” into the search box.

Click remote desktop settings.

Disable Remote Desktop by toggling "Enable Remote Desktop" off.

Click "confirm"

![image](https://github.com/DevSamLee/devsamlee.github.io/assets/96956309/b5878f22-feaf-47db-8781-e184f8f7c618)


## Suspicious Files and Hidden Folders
How can you identify a suspicious executable file? One way is by being aware of its location.

Regular Windows executable files have default folders. It is suspicious when an executable file that is named like a regular Windows process is found in the wrong folder. 

For example, if the file explorer.exe is in a directory in \Users rather than in C:\Windows.

Next, to verify if it’s the real Microsoft executable, you can check the digital signature. All official Microsoft Windows executables are signed. An unsigned "Windows" executable is a false one.

![image](https://github.com/DevSamLee/devsamlee.github.io/assets/96956309/ea09ec5f-cc38-42cf-bd5d-edd3164a77e2)
![image](https://github.com/DevSamLee/devsamlee.github.io/assets/96956309/2db09fd9-96a4-41ed-ba76-060261c64a24)

### Suspicious CPU Usage
It is also suspicious if processes use a high amount of CPU (Central Processing Unit). 

The CPU, as the name implies, handles most of the processing in a PC. In the CPU usage in Task Manager, a Windows tool that gives information about your computer's performance and all processes that are running on your computer.

Usually, you know what’s running on your computer so you should recognize the applications that show higher consumption of CPU (above 10%).

### Suspicious File Extensions
Batch files(.bat) and powershell scripts (.ps1) are usually used for automation of common tasks. They can be very powerful however, they are seldom used for distribution. 

Generally it is a good idea to investigate them and get rid of them if they are suspicious. 

When malicious actors gain access to the computer they might use scripts to execute malicious actions on the computer.
