# docker trounble shoot

* open docker then open terminal and type `docker version`
* right hand side tray `right click on docker`
* select `switch to Window container `
* you will found an error propmt with below wordings:
  
  `Containers feature is disabled. Enable it using the PowerShell script (in an administrative PowerShell)
   and restart your computer before using Docker Desktop:
   Enable-WindowOptionalFeature -  online -  FeatureName $("Microsoft-Hyper-V",  "Containers") -All`

To enable the Containers feature using PowerShell and then restart your computer, you can follow these steps:

Open PowerShell as an administrator.
Run the following command to enable the Containers feature:
powershell
Copy code
Enable-WindowsOptionalFeature -Online -FeatureName $("Microsoft-Hyper-V", "Containers") -All
After running the command, it will prompt you to restart your computer to apply the changes. Type 'Y' to confirm and press Enter.
Once your computer restarts, you should be able to use Docker Desktop with the Containers feature enabled.
Please make sure to run this command in an administrative PowerShell session to ensure it has the necessary permissions to make changes to Windows features.
  
