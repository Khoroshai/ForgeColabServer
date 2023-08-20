# Forge Minecraft Server

*This method is inspired from MineColab (https://github.com/thecoder-001/MineColab)*

*It uses free ressources thanks to Google, do not abuse of it.*

This method uses zipped saves files and zipped server folder to reduce transfer time and numbers with gdrive which improves greatly the process and might avoid the famous "Transport endpoint not connected" error caused by a kind of desync with gdrive, afaik.

The world files and logs are saved to gdrive every 5 minutes.

*Tested on 1.18.2 with around 80 mods*

# Requirements
- An open tab that will stay focused 
- A base vanilla minecraft server
- A base Forge server
- Mods
- A Playit.gg account (free)

# How to use
1) Put the base vanilla and Forge server in a folder and add the mods to it. 
2) *Zip* this folder and upload it somewhere on your gdrive.
3) *Change* the Names, Paths and the Forge command in **Initialization**.
4) *Run* only one time the first cell to set everything up.
5) (using Playit.gg) Follow the link to activate the tunnel. (You might wait a few seconds, just follow the instruction) In case it is not the first tunnel you open, you can click on *Create Tunnel* and then stop the creation as only the agent is necessary. **The URL to the server is on Playit.gg**. If the URL doesn't work, the IP should work.
6) *Launch* the **Start Server** cell as you wish. Stopping it will gently close the server. (Could raise an error but trying a second time will close normally with saving worlds, etc... in normal cases)
7) *Run* the **Stop Auto-saves** cell when the server is stopped. You can run it while the server is up to make it auto-run when the server stops.
8) (optional) You can run the very last cell to save any changes made to the server. (properties, config...)

# Additional informations

*MineColab* has a cell to create the base server on gdrive. You can run it and then download the folder to continue the creation (Forge + mods + zipping)

To create the base Forge server, as of August 2023, you can execute a jar file found on their official website.

The *run.sh* file, that you'll get with the Forge base, contains a command which includes a version that you'll compare with *forgeCommand* at **Initialization**.

The tunnel used in this Notebook is Playit but you can easily copy-paste Ngrok or Argo from *MineColab*. Just pay attention to the command slighty modified here.

A Kaggle version of this notebook is available here : https://github.com/Khoroshai/ForgeKaggleServer. Kaggle processor is slightly better but setup is less intuitive.

# Known issues

- The **Stop Auto-saves** cell takes up to 5 minutes (saving interval) to complete. Run, stop, run is a work around by raising an error.
*Solution found in the Kaggle version*.

- Sometimes the server console stops allowing inputs. This happens when the bottom timer also stops counting the running time despite the server being up. Maybe merge to the same methods as the Kaggle version.

# To do

- Add Ngrok and Argo.
- Add improvments from the Kaggle version.
