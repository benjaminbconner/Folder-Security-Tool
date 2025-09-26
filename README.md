# Folder-Security-Tool

Here's a PowerShell script that implements your Folder Security Tool with a simple menu interface. It allows users to:

Create a Project folder.

Create a Proposal folder.

Grant access to a Project folder.

Grant access to a Proposal folder.

You can customize folder paths and user/group names as needed.

🛠 Notes
This script uses NTFS permissions via Set-Acl.

You must run it with administrative privileges to modify folder permissions.

You can extend it to include logging, error handling, or GUI elements if needed.

To package your PowerShell script into an executable .exe file, you'll need to use a tool that wraps PowerShell scripts into executables. Here's a step-by-step guide using PS2EXE, a popular and free option:

🧰 Step-by-Step: Convert PowerShell Script to EXE
1. Install PS2EXE
You can install it via PowerShell Gallery:

Install-Module -Name ps2exe -Scope CurrentUser
If prompted to trust the repository, type Y and press Enter.

3. Save Your Script
Save your Folder Security Tool script as a .ps1 file, for example:
FolderSecurityTool.ps1

3. Convert to EXE
Run the following command to convert your script:
Invoke-PS2EXE -InputFile "FolderSecurityTool.ps1" -OutputFile "FolderSecurityTool.exe"
You can also add optional parameters:

-NoConsole for GUI apps

-IconFile to add a custom icon

-Title to set the window title

4. Test the EXE
Double-click the generated .exe file to run your Folder Security Tool. Make sure to run it as Administrator if you're modifying NTFS permissions.
