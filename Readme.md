#Composer integration for Sublime Text 2
With this plugin you can manage your dependencies with [composer](http://www.getcomposer.org/)

Currently the following features are supported:
* Execute composer install
* Execute composer update
* Execute composer self-update
* Package management:
  * Remove package
* Edit composer.json file


##Instalation
### Via Package Control
First install [Package Control](http://wbond.net/sublime_packages/package_control/installation) if you haven't done so yet.

Then go to Preferences -> Package Control -> Install Package and type **composer** to install this plugin.

This is the recommended installation method.
### Manual Instalation
Go to your sublime package folder and type:
```git clone git@github.com:francodacosta/composer-sublime.git```

##Running Composer
Just open the command prompt (ctrl + shifp + p) and type composer, context menus are also provided

##Features Help
###Composer install
executes the composer install command, with the default settings the following command will be executed

```composer.phar install -n -v```

###Composer update
executes the composer update command, with the default settings the following command will be executed

```composer.phar update -n -v```

###Composer self update
executes the composer self update command, updating the composer binary to the latest version.
With the default settings the following command will be executed

```composer.phar self-update -n -v```

###Composer Add Package
You can add a package to the required package list.

When you execute this command a prompt is presented (in the bottom of the screen) allowing you to specify the package name and version contraints

The syntax for adding a package is as follows:

```package name : version```

if you do not specify a version the default will be ```*```

###Composer Remove Package
Removes a package from the required packages section in *composer.json*

When you select this option a list of required packages will pop up, you only need to select the package to be removed

###Edit composer.json file
this option will open a new window pointing to the composer.json file

##Configuration Options

* __show_status__: show messages in the status bar
* __show_output__: opens an output window and shows composer working
* __composer_command__:  Path to composer.phar file
* __composer_install_extra__: extra arguments to pass to the *install* command
* __composer_update_extra__: extra arguments to pass to the *update* command
* __composer_selfupdate_extra__: extra arguments to pass to the *self-update* command

##How is composer.json found?
The plugin tries to locate the *composer.json* file. It starts at the same folder of the file beeing edited and goes all the way up to the root folder.
If you do not specify the __composer_command__ option the default is to look for *composer.phar* on the same folder where *composer.json* was found
