# Installing OEM Unleashed
 - In order to achieve the look and feel of the original MS dashboard you will have to add our theme and update the main config.xml file located at C:\config.xml.
 - To update the config.xml open the file in your XML editor of choice.
 - Locate the Menu section and replace the entire contents of the menu section with the code below.
```
	<Menu>
		<List Text="XBMC" Sort="Off" Batch="True">
			<Item Action="rename" Arg1="E:\Shortcuts\XBMC Shortcut\xbmc.xbe" Arg2="E:\Shortcuts\XBMC Shortcut\xbmc.tmp">XBMC or shortcut not installed. Use HeXEn to install XBMC.</Item>
			<Item Action="rename" Arg1="E:\Shortcuts\XBMC Shortcut\xbmc.tmp" Arg2="E:\Shortcuts\XBMC Shortcut\xbmc.xbe"></Item>
			<Item Action="E:\Shortcuts\XBMC Shortcut\xbmc.xbe">XBMC</Item>
		</List>
		<Item Action="LaunchDVD">LAUNCH DVD</Item>
		<List Text="GAMES" Sort="On" Auto="On">
			<Path>E:\Games</Path>
			<Path>F:\Games</Path>
			<Path>G:\Games</Path>
		</List>
		<List Text="PC GAMES" Sort="On" Auto="On">
			<Path>E:\PCGames</Path>
			<Path>F:\PCGames</Path>
			<Path>G:\PCGames</Path>
		</List>
		<List Text="APPLICATIONS" Sort="On" Auto="On">
			<Path>E:\Apps</Path>
			<Path>F:\Apps</Path>
			<Path>G:\Apps</Path>
		</List>
		<List Text="EMULATORS" Sort="On" Auto="On">
			<Path>F:\Emulators</Path>
			<Path>G:\Emulators</Path>
		</List>
		<List Text="HOMEBREW GAMES" Sort="On" Auto="On">
			<Path>F:\Homebrew</Path>
			<Path>G:\HomeBrew</Path>
		</List>
		<List Text="GAME MANAGEMENT" Sort="Off" Auto="On">
			<Item Action="SavesManager">Game Saves Manager</Item>
			<Item Action="E:\Apps\DVD2Xbox\default.xbe">Copy Game Disc</Item>
		</List>
		<List Text="XBOX ADMIN" Sort="Off" Auto="On">
			<List Text="DASHBOARDS" Sort="Off" Auto="On">
				<Item Action="C:\Xboxdash.xbe">MS Dashboard</Item>
				<Item Action="E:\Dash\EvolutionX\evoxdash.xbe">EvolutionX</Item>
				<Item Action="E:\Dash\UnleashX\unleashx.xbe">UnleashX</Item>
			</List>
			<List Text="CLEAR CACHE" Sort="Off" Batch="True">
				<item action="messagebox" arg1="Clear Cache">This will clear your cache. It can be helpful when you experience games not loading or crashing.</item>
				<Item Action="Format" Arg1="X"></Item>
				<Item Action="Format" Arg1="Y"></Item>
				<Item Action="Format" Arg1="Z"></Item>
				<Item Action="copy" Arg1="E:\Dash\UnleashX\unleashx.xbe" Arg2="E:\cache\Default.xbe"></Item>
				<Item Action="delete" Arg1="e:\cache"></Item>
				<item action="messagebox" arg1="Completed">Cache is cleared.</item>
			</List>
			<List Text="SYSTEM" Sort="On" Auto="On">
				<Item Action="Skins">SKINS</Item>
				<Item Action="Settings">SETTINGS</Item>
				<List Text="NETWORK CONTROL" Sort="Off" Auto="On">
					<Item Action="FTPStop">STOP FTP</Item>
					<Item Action="FTPStart">START FTP</Item>
					<Item Action="FTPReset">RESET FTP</Item>
					<Item Action="NETReset">RESTART NETWORK</Item>
				</List>
				<List Text="TRAY CONTROL" Sort="Off" Auto="On">
					<Item Action="TrayClose">CLOSE DVD TRAY</Item>
					<Item Action="TrayOpen">OPEN DVD TRAY</Item>
				</List>
				<Item Action="FileManager">FILE EXPLORER</Item>
			</List>
			<Item Action="SetClock">SET CLOCK</Item>
		</List>
		<Item Action="Restart">REBOOT</Item>
		<Item Action="Shutdown">SHUTDOWN</Item>
	</Menu>
```
 - Once the file is updated, save it.
 - Upload the modified file to the root of your C drive.
  - Enjoy the look and feel of a stock dashboard with the featurs of a modded dash!

# Optional Changes
# Changing the Screensaver
 - In the same config file above locate the line

```
			<Skin Path="E:\Dash\Unleashx\Skins">UnleashedX</Skin>
```

And cange it to:

```
			<Skin Path="E:\Dash\Unleashx\Skins">OEM Unleashed</Skin>
```

This will change your screensaver to call out the name of the dashboard.

# Data Display options
 - If you want to have a clean version of the dash, ie not displaying any data.  Delete the Skins.xml file and copy/paste then rename Clean-Skins.xml to Skins.xml.
 - If you want a version that shows the MB and CPU temps, delete the Skins.xml file and copy/paste then rename Temps-Skins.xml to Skins.xml.
 - If you want to restore the origial design, delete the Skins.xml file and copy/paste then rename Standard-Skins.xml to Skins.xml.