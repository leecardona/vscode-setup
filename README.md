> Table of Contents
- [Overview](https://github.com/leecardona/vscode-setup/tree/development#overview)
- [Setup Steps](https://github.com/leecardona/vscode-setup/tree/development#setup-steps)
  - [Base Setup](https://github.com/leecardona/vscode-setup/tree/development#base-setup)
  - [Setup Git Repo](https://github.com/leecardona/vscode-setup/tree/development#setup-git-repo)
  - [Setup Workspace](https://github.com/leecardona/vscode-setup/tree/development#setup-workspace)
  - [Adding Tag Extention](https://github.com/leecardona/vscode-setup/tree/development#adding-extention-for-tag-automation)
- [Workflow Steps](https://github.com/leecardona/vscode-setup/tree/development#workflow-steps)
  - [Committing Code](https://github.com/leecardona/vscode-setup/tree/development#committing-code-and-updating-remote-repo)
  - [Managing Tags](https://github.com/leecardona/vscode-setup/tree/development#managing-tags)
    - [Create Tag](https://github.com/leecardona/vscode-setup/tree/development#create-tag)
    - [List Tags](https://github.com/leecardona/vscode-setup/tree/development#list-tags)
  - [Creating Branches](https://github.com/leecardona/vscode-setup/tree/development#creating-branches)
  - [Switching Branches](https://github.com/leecardona/vscode-setup/tree/development#switching-branches)
  - [Merging Branches](https://github.com/leecardona/vscode-setup/tree/development#merging-branches)
  - [Deleting Branches](https://github.com/leecardona/vscode-setup/tree/development#deleting-branches)
- [Contributing](https://github.com/leecardona/vscode-setup/tree/development#contributing)
- [Copyright](https://github.com/leecardona/vscode-setup/tree/development#copyright)
- [License](https://github.com/leecardona/vscode-setup/tree/development#license)


# Overview:
Documentation of steps taken to setup and use Visual Studio Code for development on a Mac environment


# Setup Steps:
Below are the steps required, *with some optional steps* , to setup a working VSC environment. These step are typically only performed once.

## Base Setup:
- [X] Download Visual Studio Code (VSC) from https://code.visualstudio.com/
- [X] Once installed and started you will be welcomed by the `Welcome` screen

![vscode welcome screen](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_welcome_scrn.png?raw=true)

## Setup git repo:
- [X] Launch command prompt with keyboard shortcut `shift+cmd+p`

![vscode cmd prompt](https://raw.githubusercontent.com/leecardona/vscode-setup/master/assets/vscode_cmd_prompt.png)
- [X] Inside the cmd prompt, enter the `Git: Clone` cmd or select it from the dropdown list of common/recent cmds
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

- [X] Once you have named and saved your workspace, note the updated VSC Explorer as it now will denote that the repo is saved as a `(WORKSPACE)`

![repo is a workspace in explorer](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_workspace_in_explorer.png?raw=true)

## Adding Extention for Tag Automation:
*Optional:* Git tags are used to denote key points in code development that signify a milestone, typically a release of some kind like a major or minor release version, or hotfix. Git hosting services like Github will detect tags and auto create releases for you with nice zipped file links for easy release downloading for end-users. VSC support plugins/extentions that add easy to use features to the user interface of VSC that can make activities like tagging easier to manage. 

- [X] Go to the VSC Marketplace to search and install available extentions. Enter the keyboard shortcut `cmd + p` Note this brings up the quick actions dialog not the VSC cmd prompt - they are not the same.

![vscode actions dialog](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_action_cmd_prompt.png?raw=true)

- [X] Once presented with the actions dialog enter: `ext install git-tags`. I thought this would install the extention but it did not. It only navigated me to the VSC Marketplace and filtered the search for tag related extentions, just be aware. 

- [X] You can also select the VSC Marketplace tab to manually navigate and then enter `tags` in the search box.

![VSC marketplace](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_marketplace.png?raw=true)

- [X] From the result of tag related extentions select `git-tag` by clicking on the `install` button for it.


# Workflow Steps:
Below are steps that are performed as part of using VSC on a normal iterative basis.

## Committing code and updating remote repo:
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

## Managing tags:
- [X] To manage tags using the git-tag extention simply navigate to the SCM tab:

![vscode SCM tab](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_src_ctr_tab.png?raw=true)

- [X] Select the `More actions` icon:

![commit more actions icon](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_commit_actions.png?raw=true)

### Create tag

- [X] To add a tag to the current commit, select `Create tag` from the dropdown menu:

![Create tag](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_create_tag.png?raw=true)

- [X] This will result in a create tag input dialog box opening:

![enter tag dialog box](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_enter_tag.png?raw=true)

- [X] Enter your desired tag value and press enter. You will then be prompted for syncing your remote repo with this tag at this time or not. Normally select `Yes` to complete this operation.

![sync tag?](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_sync_tag.png?raw=true)

### List tags:

- [X] Git-tag extention also allows to quickly view all your tags and even delete them if you so desire. To view your tags navigate to the SCM tab:

![vscode SCM tab](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_src_ctr_tab.png?raw=true)

- [X] Select the `More actions` icon:

![commit more actions icon](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_commit_actions.png?raw=true) 

- [X] To view your tags, select `List tags` from the dropdown menu:

![List tag](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_list_tags.png?raw=true)

- [X] This will result in a tags list window opening as shown below:

![tags window](https://github.com/leecardona/vscode-setup/blob/master/assets/vscode_list_tags_list.png?raw=true)

- [X] From here you can view all your tags as well as `DELETE` any you wish to remove

## Creating Branches:
- [X] Creating branches in VSC is pretty easy and is done via the branch switching dialog. To bring up the branch switching dialog click on the current banch indicator at the bottom left of VSC screen:

![vscode branch selector](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_branch_selector.png?raw=true)

- [X] This will result in the branch switching dialog as shown below:

![vscode branch switcher](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_branch_dialog_menu.png?raw=true)

- [X] From here simply click on the `+ Create new branch` option and you'll be presented with an input box to enter your desired branch name:

![vscode branch name input](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_new_branch_name.png?raw=true)

- [X] VSC also automatically switches you to the new branch once created. You can verify this by noting the current branch indicator at the lower left of the VSC screen:

![vscode new branch](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_new_branch.png?raw=true)

- [X] After the new branch is created be sure to update the remote repo by publishing this change. Simply click the update cloud icon to the right of the current branch indicator to update the remote repo with the new branch:

![publish changes to remote](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_publish_changes.png?raw=true)

## Switching Branches:
- [X] Switching branches in VSC is pretty easy and is done via the branch switching dialog. To bring up the branch switching dialog click on the current banch indicator at the bottom left of VSC screen:

![vscode branch selector](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_branch_selector.png?raw=true)

- [X] This will result in the branch switching dialog as shown below:

![vscode branch switcher](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_branch_dialog_menu.png?raw=true)

- [X] From here simply select the desired branch from the list of available branches and VSC will automatically switch you to that branch

## Merging Branches:
- [X] Merging branches to pretty straight forward as well. First ensure you are in the `target` branch you want to update, _**not the `source` branch with the new code and/or files**_ . You can check the current banch by looking at the current branch indicator at the bottom left of VSC screen:

![vscode branch selector](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_branch_selector.png?raw=true)

- [X] To initiate a merge use the keyboard shortcut combination `shift+cmd+p` to bring up the VSC command prompt:

![vscode merge dialog](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_merge-cmd.png?raw=true)

- [X] Inside the cmd prompt, enter the `Git: Merge Branch` cmd or select it from the dropdown list of common/recent cmds. This will result in the `Select a branch to merge from` dialog appearing. 

![select branch to merge](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_merge_from_dialog.png?raw=true)

- [X] Select your `source` branch from the list of available branches to update the `target` branch you are currently in.

## Deleting Branches:
- [X] To delete a branch in VSC you have to first ensure you are not currently in the branch you wish to delete or you wont be able to select it for deletion. You can check the current banch by looking at the current branch indicator at the bottom left of VSC screen:

![vscode branch selector](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_branch_selector.png?raw=true)

- [X] Once you're sure your not in the branch you wish to delete, enter the keyboard shortcut combination `shift+cmd+p` to bring up the VSC command prompt:

![vscode merge dialog](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_merge-cmd.png?raw=true)

- [X] Inside the cmd prompt, enter the `Git: Delete Branch` cmd or select it from the dropdown list of common/recent cmds. This will result in the `Select a branch to delete` dialog appearing. 

![select branch to merge](https://github.com/leecardona/vscode-setup/blob/development/assets/vscode_delete_branch.png?raw=true)

- [X] Select the branch from the list of available branches you wish to delete.

### Contributing
I welcome and appreciate community contributions. If you have an idea or a question I'd love to hear from you! The easiest ways to contribute is by forking this repo followed by a pull request or raising an issues in this repo's Github.

### Copyright
Copyright 2018 Lee Cardona. @leecardona

### License
The documentation is provided under Apache License 2.0. Contributions to this project are accepted under the same license.

