# docker trounble shoot

* open docker then open terminal and type `docker version`

C:\Users\Asif sb>docker version

Client:

 Cloud integration: v1.0.35+desktop.11
 
 Version:           25.0.3
 
 API version:       1.44
 
 Go version:        go1.21.6
 
 Git commit:        4debf41
 
 Built:             Tue Feb  6 21:13:02 2024
 
 OS/Arch:           windows/amd64
 
 Context:           default
 


Server: Docker Desktop 4.28.0 (139021)

 Engine:
 
  Version:          25.0.3
  
  API version:      1.44 (minimum version 1.24)
  
  Go version:       go1.21.6
  
  Git commit:       f417435
  
  Built:            Tue Feb  6 21:14:25 2024
  
  OS/Arch:          linux/amd64
  
  Experimental:     false
  
 containerd:
 
  Version:          1.6.28
  
  GitCommit:        ae07eda36dd25f8a1b98dfbf587313b99c0190bb
  
 runc:
 
  Version:          1.1.12
  
  GitCommit:        v1.1.12-0-g51d5e94
  
 docker-init:
 
  Version:          0.19.0
  
  GitCommit:        de40ad0
  
* right hand side tray `right click on docker`
* ![image](https://github.com/imransecrets/docker/assets/8496861/8428c08c-65cf-4008-813a-ed6cf4bafc8e)

* select `switch to Window container `
* you will found an error propmt with below wordings:
  
  `Containers feature is disabled. Enable it using the PowerShell script (in an administrative PowerShell)
   and restart your computer before using Docker Desktop:
   Enable-WindowOptionalFeature -  online -  FeatureName $("Microsoft-Hyper-V",  "Containers") -All`

To enable the Containers feature using PowerShell and then restart your computer, you can follow these steps:

Open PowerShell as an administrator.
Run the following command to enable the Containers feature:

`Enable-WindowsOptionalFeature -Online -FeatureName $("Microsoft-Hyper-V", "Containers") -All`

After running the command, it will prompt you to restart your computer to apply the changes. Type 'Y' to confirm and press Enter.
Once your computer restarts, you should be able to use Docker Desktop with the Containers feature enabled.
Please make sure to run this command in an administrative PowerShell session to ensure it has the necessary permissions to make changes to Windows features.
  
