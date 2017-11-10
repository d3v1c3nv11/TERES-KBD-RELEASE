How to update the touchscreen button firmware:

Download and extract the tgz archive. Open a console and navigate to the folder where you placed the archive then extract with the follwing command:

```bash
tar -xvf firmware.tar.gz
```
navigate to the firmware folder and then perform an update with the following commands: 
```bash
cd firmware 
sudo ./update 
```
Then follow the onscreen prompts: 

Type the sudo password. 

Then press Fn+TuXkey+escape together to
start the update.

The firmware should now be updated.


Note: You must add keyboard shortcut with name Suspend and command: "systemctl suspend" activated with key Fn+F1
