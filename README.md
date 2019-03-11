# Rider settings repository
Jetbrains rider settings shared across systems

### Prerequisite
Before you start configuring a settings repository, make sure that the Settings Repository plugin is enabled in the Settings/Preferences dialog (⌘ ,) under Plugins.

### Useage
This allows you to sync any configurable components of your jetbrains desktop tools

### Setup
* Create a Git repository on any hosting service, such as Bitbucket or GitHub.
* On the computer where the JetBrains Rider instance whose settings you want to share is installed, select File | Settings Repository from the main menu. Specify the URL of the repository you've created and click Overwrite Remote.
* On each computer where you want your settings to be applied, In the Settings/Preferences dialog (⌘ ,), expand the Tools node and choose Settings Repository. Specify the URL of the repository you've created, and click Overwrite Local.
You can click Merge if you want the repository to keep a combination of the remote settings and your local settings. If any conflicts are detected, a dialog will be displayed where you can resolve these conflicts.
* If you want to overwrite the remote settings with your local settings, click Overwrite Remote.
* Your local settings will be automatically synchronized with the settings stored in the repository each time you perform an Update Project or a Push operation, or when you close your project or exit JetBrains Rider.
* On the first sync, you will be prompted to specify a username and password. It is recommended to use an access token for GitHub authentication. If, for some reason, you want to use a username and password instead of an access token, or your Git hosting provider doesn't support it, it is recommended to configure the Git credentials helper.

### Shortcut map
⌘E : Extract Interface
⌘I : Implementation
⌘D : Declaration

### Jetbrains file structure
Mac OS X
Configuration (idea.config.path):
* ~/Library/Preferences/<PRODUCT><VERSION>
Caches (idea.system.path):
* ~/Library/Caches/<PRODUCT><VERSION>
Plugins (idea.plugins.path):
* ~/Library/Application Support/<PRODUCT><VERSION>
Logs (idea.log.path):
* ~/Library/Logs/<PRODUCT><VERSION>
