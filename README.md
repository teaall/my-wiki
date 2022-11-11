# Custom Wiki for Software Developers

<div align="center">
  <img src="logo.png" alt="Wiki.js" width="600" />
</div>

This wiki serves as a personal collection of information of principles, techniques and commands of software development.
It's based on the open source project [WikiJs](https://github.com/requarks/wiki). and can be locally deployed using docker. :rocket:

## Getting Started

Start the containers using the `docker-compose` file located in `local_setup`. Set up your user mail and user password.

---

Now you'll have to configure Wiki.js to sync with this repo.

1. In the Administration Area, click on Storage in the left navigation menu.
2. Make sure the Git storage target is checked.
3. Click on the Git tab.
4. Enter the following settings:

- Authentication Type: ssh
- Repository URI: git@github.com:teaall/my-wiki.git
- Branch: main
- SSH Private Key Mode: contents
- B - SSH Private Key Contens: Content of the `local_setup/wiki-user` file
- Username: Empty
- Password: Empty
- Default Author Email: Should match your GitHub account email.
- Default Author Name: Should match your GitHub account name.
- Local Repository Path: Choose where the repo will be cloned locally or leave the default ./data/repo value.
- Verify SSL Certificate: On

5. Set the Sync Direction to Pull from target.
6. Set the Sync Schedule to your preffered time
7. Click the Apply Changes button at the top of the page.
8. Wait for the Status panel to update. A new entry for Git should appear in green. If the bar is red, it means you have an error in your configuration. Go back to the Git tab, fix the error and try again.

> :exclamation: The private ssh key has only read rigths, so any changes will only be saved on your local machine

If you feel like branching from this state create your own github repository to securely save your files. ([see also](https://docs.requarks.io/storage/git))
