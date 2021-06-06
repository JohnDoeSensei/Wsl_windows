# Wsl_windows


<p> Windows Subsystem for Linux (WSL) est une couche de compatibilité permettant d'exécuter des exécutables binaires Linux (au format ELF) de manière native sur Windows 10 et Windows Server 2019. </p>
<p> La première version de WSL fournit une interface noyau compatible Linux développée par Microsoft, qui ne contient aucun code source du noyau Linux6. Cette interface permet d'exécuter un espace utilisateur GNU comme celui d'Ubuntu7,8,9,10, openSUSE11, SUSE Linux Enterprise Server12,13,14, Debian15 ou Kali Linux16. Un tel espace utilisateur peut contenir un shell Bash avec des outils en ligne de commande GNU / Linux natifs (sed, awk, etc.), des interpréteurs de langage de programmation (Ruby, Python, etc.) et même des applications graphiques (utilisant un serveur X11 côté hôte)17. </p>

L'architecture a été repensée dans WSL 21, avec un noyau Linux s'exécutant dans une machine virtuelle légère. 
  
 </p>
  
## Installation 
 
source: https://docs.microsoft.com/fr-fr/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package
 
* Open Powershell in admin mode and type :
 
<code> dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all </code>
 
* Just reboot your computer. For activate version2 of WSL, just type :
 
<code> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all </code>
  
* Download from Microsoft store any distribution linux like Ubuntu, Debian or Kali. 
Or if you need specific distribution type : 

<code> wsl --list --online </code>
<code> wsl --install -d DistributionName </code>
  
  
And check his WSL version with :
 
<code> wsl --list --verbose </code>

If your distro Ubuntu-20.04 is in version 1, just type that to update version 2 :

<code> wsl --set-version Ubuntu-20.04 2 </code>

You can obtain wsl version 2 by default in future with this command 

<code> wsl --set-default-version 2 </code>
 
* If you have problem when you launch your distribution linux, just download update package for kernel linux here : https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi and execute it.
 
 
 
