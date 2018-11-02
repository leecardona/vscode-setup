# vscode-setup
Documentation of steps taken to setup Visual Studio Code development environment (Mac version)

## Base Setup:
- [X] Download Visual Studio Code (VSC) from https://code.visualstudio.com/
- [X] Once installed and started you will be welcomed by the `Welcome` screen

![vscode welcome screen](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_welcome_scrn.png?raw=true)

## Setup git repo:
- [X] Launch command prompt with keyboard shortcut `shift+cmd+p`

![vscode cmd prompt](https://raw.githubusercontent.com/leecardona/vscode-setup/master/assets/vscode_cmd_prompt.png)
- [X] Inside the cmd prompt, enter the `Git: Clone` cmd or select it from the downdown list of common/recent cmds
- [X] This will prompt you for your `repo url` e.g. `https://github.com/leecardona/vscode-setup.git` 

![repo url prompt](https://github.com/leecardona/vscode-setup/blob/master/assets/repo_url_prompt.png?raw=true)
- [X] After you provide the url and hit enter, you will be presented with a download save dialog box asking you to designate where on your local machine you wish to place this local copy of the repo
- [X] Once the repo is done downloading, VSC will prompt you on the lower right with post repo download action shorcuts, select `Open repository` option 

![Repo Action shortcuts](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_post_repo_add_actions_dialog.png?raw=true)
- [X] You should now be navigated to the source control management (SCM) tab in VSC. You can also manually select this tab by clicking on the SCM tab icon 

![vscode SCM tab](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_src_ctr_tab.png?raw=true)

## Setup Workspace
This is an optional step but I found that VSC on Mac did not always detect file changes done on the local machine via the finder or if your repo is on a cloud drive like Google Drive or Dropbox. Creating a designated Workspace seems to address this issue. Typically a Workspace is used when you want to save the setup of you VSC working environment. For example, if your project is comprised of more than one repo folder or perhaps in addition to your primary repo folder you want to include some additional folders for quick access via the VSC file explorer tree.

- [X] Ensure you're in the desired repo by selecting the `Explorer` tab

![explorer tab](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_explorer_tab.png?raw=true)

- [X] You should see your repo and it's folder structure in the Explorer tree

![repo in explorer](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_explorer_tree.png?raw=true)

- [X] from the File menu, select `Save Workspace As...`

![save workspace as](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_save_workspace.png?raw=true)

- [X] You will be prompted with a local finder dropdown box to select where on your local machine you wish to save the workspace config file

![save workspace dialog](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_save_workspace_dialog_box.png?raw=true)

- [X] Once you have named and saved you workspace, note the updated VSC Explorer as it now will denote that the repo is saved as a `(Workspace)`

![repo is a workspace in explorer](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_workspace_in_explorer.png?raw=true)
