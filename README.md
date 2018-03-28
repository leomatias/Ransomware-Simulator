# Ransomware-Simulator
#### The Simulation ####
These scripts will encrypt and decrypt files using a certificate installed on the computer from which they are run.

To check if you have a certificate installed run this command from an administrative powershell prompt:

get-childitem cert:\currentuser\my

The thumbprint id of the cert is needed in both scripts. Copy the thumbprint id to each script as outlined in the 

script. Example:
#define the cert to use for encryption
$Cert = $(Get-ChildItem Cert:\CurrentUser\My\THUMBPRINTGOESHERE)

####Disclaimer, this script will encrypt files so make sure you have a backup of the files before running the 

script.####

The script will encrypt files on the lowest drive letter (Z:). The decrypt script also decrypts files on the lowest 

drive letter. These scripts are meant for testing purposes only and should not be used in any unethical or malicious 

manner.

