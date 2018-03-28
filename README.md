# Ransomware-Simulator
Description:
We have written two PowerShell scripts which act as the ransomware simulator. One script encrypts the data, and the other script decrypts the data using a public/private key pair. We created these as a tool, so that you can test your defenses against actual ransomware. The purpose of the decrypter, is to ensure that your files aren’t permanently destroyed.

#### How it works ####
  - The network drives are enumerated and sorted in descending order.
  - The lowest drive letter will be attacked. This gives you the ability to control what shares are affected. Its recommended to only have     one drive (Z:) mapped while you run the scripts.
  - Each file on the share(s) will be encrypted with the Public key of the certificate. 
  - You will need a certificate for this to work. Your computer probably has one already, and we've included all the necessary steps           below.
  - After all the files have been encrypted, the script exits.

#### Running The Simulation ####
These scripts will encrypt and decrypt files using a certificate installed on the computer from which they are run.

To check if you have a certificate installed run this command from an administrative powershell prompt:

get-childitem cert:\currentuser\my

The thumbprint id of the cert is needed in both scripts. Copy the thumbprint id to each script as outlined in the 

script. Example:
#define the cert to use for encryption
$Cert = $(Get-ChildItem Cert:\CurrentUser\My\THUMBPRINTGOESHERE)

#### DISCLAIMER ####
The script will encrypt files so make sure you have a backup of the files before running.

These scripts are meant for testing purposes only and should not be used in any unethical or malicious manner.

