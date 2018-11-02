# vscode-setup
Documentation of steps taken to setup and use a Visual Studio Code development environment (Mac version)


# Setup Steps
Below are the steps required, *with some optional steps* , to setup a working VSC environment. These step are typically only performed once.

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
*Optional:* This is an optional step but I found that VSC on Mac did not always detect file changes done on the local machine via the finder or if your repo is on a cloud drive like Google Drive or Dropbox. Creating a designated Workspace seems to address this issue. Typically a Workspace is used when you want to save the setup of you VSC working environment. For example, if your project is comprised of more than one repo folder or perhaps in addition to your primary repo folder you want to include some additional folders for quick access via the VSC file explorer tree.

- [X] Ensure you're in the desired repo by selecting the `Explorer` tab

![explorer tab](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_explorer_tab.png?raw=true)

- [X] You should see your repo and it's folder structure in the VSC Explorer

![repo in explorer](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_explorer_tree.png?raw=true)

- [X] from the File menu, select `Save Workspace As...`

![save workspace as](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_save_workspace.png?raw=true)

- [X] You will be prompted with a local finder dropdown box to select where on your local machine you wish to save the workspace config file

![save workspace dialog](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_save_workspace_dialog_box.png?raw=true)

- [X] Once you have named and saved youR workspace, note the updated VSC Explorer as it now will denote that the repo is saved as a `(WORKSPACE)`

![repo is a workspace in explorer](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_workspace_in_explorer.png?raw=true)

## Adding Extention for Tag Automation
*Optional:* Git tags are used to denote key points in code development that signify a milestone, typically a release of some kind like a major or minor release version, or hotfix. Git hosting services like Github will detect tags and auto create releases for you with nice zipped file links for easy release downloading for end-users. VSC support plugins/extentions that add easy to use features to the user interface of VSC that can make activities like tagging easier to manage. 

- [X] Go to the VSC Marketplace to search and install available extentions. Enter the keyboard shortcut `cmd + p` Note this brings up the quick actions dialog not the VSC cmd prompt - they are not the same.

![vscode actions dialog](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_action_cmd_prompt.png?raw=true)

- [X] Once presented with the actions dialog enter: `ext install git-tags`. I thought this would install the extention but it did not. It only navigated me to the VSC Marketplace and filtered the search for tag related extentions, just be aware. 

- [X] You can also select the VSC Marketplace tab to manually navigate and then enter `tags` in the search box.

![VSC marketplace](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_marketplace.png?raw=true)

- [X] From the result of tag related extentions select `git-tag` by clicking on the `install` button for it.


# Workflow Steps
Below are steps that are performed as part of using VSC on a normal iterative basis.

## Committing code and updating remote repo
Commiting code updates is pretty straight forward in VSC as it should auto detect any changes to your local git repo. When it does, VSC will provide a visual indication by placing a badge over the SCM tab icon denoting how many changes it has deteced, like so:

![change detection indicator](https://github.com/leecardona/vscode-setup/blob/master/assets/change_detected.png?raw=true)

- [X] To commit changes select the SCM tab and you be presented with the commit box as shown below:

![commit box](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_src_ctrl_chg_commit.png?raw=true)

- [X] To locally commit your changes simply enter a commit message in the provided box and then click on the `Check Mark` above the message box:

![checkin commit](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_commit_checkmark.png?raw=true)

- [X] Once your changes have been commited you are able to push or sync your changes with the remote repo or perform other actions by selecting the `More actions` icon, represented by an elipse icon:

![commit more actions icon](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_commit_actions.png?raw=true)

- [X] This will result in the actions dropdown dialog appearing. From here simply select the git action you wish to perform for this commit, e.g. push, pull, sync, other...

![list of git commit action](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_commit_actions_list.png?raw=true)

