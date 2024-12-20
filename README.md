Fork of https://github.com/schtritoff/hyperv-vm-provisioning with 4 new parameters which were needed for my use cases:

\- InstallPowerShell:\
      Install PowerShell into the VM as well.
  
\- PrintUserDataOnly:\
      Only prints the generated cloud init userdata file but doesn't actually create the VM.
      Useful when troubleshooting or modifying the script.
      You can valdiate the cloud-init data by saving it into a file and running this command:
      ```
          cloud-init schema --config-file "filename.yaml"
      ```
  
\- AddKeyToRoot:\
      Add the SSH key specified with -GuestAdminSshPubKeyFile to the root user's authorized_keys file.
      Warning: Only recommended for local environment.
  
\- RootPassword:\
      Specify a password for the root user. Not recommended.
