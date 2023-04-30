# Open in Visual Studio Code

- Open Automator
- Create a new document
- Select Quick Action
- Set “Service receives selected” to `files or folders` in `any application`
- Add a `Run Shell Script` action
   - your default shell should already be selected, otherwise use `/bin/zsh` for macOS 10.15 (”Catalina”) or later
   - older versions of macOS use `/bin/bash`
   - if you're using something else, you probably know what to do :wink:
- Set the script action to the following
   ```
   for f in "$@"; do
     open -a 'Visual Studio Code' "$@"
   done
   ```
   
- Set “Pass input” to `as arguments`
- Save as `Open in Visual Studio Code`

# Keyboard Shortcuts

You can assign a global shortcut to run the services we just created

- Open “System Preferences”
- Select “Keyboard” then the “Shortcuts” tab
- In the left pane, click on “Services”
- In the right pane, scroll to  “Files and Folders”
- Select “Open in Visual Studio Code” click “add shortcut”
- Select a shortcut

# Edit Context Menu items

You might want to rename or edit the items we just created

- Activate Finder
- Click on “Finder” in the Apple menu, select “Services” then “Services Preferences”
- In the right pane, scroll to  “Files and Folders” and scroll to the item you want to edit
- Right click the item and select “Open in Visual Studio Code”
- Edit and save

Alternatively, you can edit the workflow (e.g. `~/Library/Services/Open in Visual Studio Code.workflow`) in your preferred text editor 