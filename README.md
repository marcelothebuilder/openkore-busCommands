# openkore-busCommands
> Openkore plugin.
With busCommands you can send console commands to your bots with various options.

## Installation

For Openkore and BetaKore, clone this repository at the following folder:
```
<openkore>/plugins/
```

## Usage example

### sys.txt

Please turn on bus flag to 1 inside control/sys.txt before using this plugin.

### Console

```
bus <all|bot nickname|field name> <console command>
```
If you used "all", the command will be run in all openkore instances using this plugin.
If you used "bot nickname", only the character with the nickname typed will run the command.
And if you used "field name", only bots inside that field will run the command.

You can also use this plugin in messenger mode. That way you can send ANY kind of message and work with them inside your macro plugin.
First set MESSENGER_MODE to 1. Now the plugin won't run the "commands", instead it will only receive them and call the hook bus_received.

### Macro example
```
automacro bustest {
	hook bus_received
	save message
	call {
		log just received $.hookSave0 from busCommands in messenger mode
	}
}
```

## Release History

* 0.0.1
    * Initial release.

## More info

Distributed under the GNU GENERAL PUBLIC LICENSE Version 3 license. See ``LICENSE`` for more information.

[https://github.com/marcelothebuilder/](https://github.com/marcelothebuilder/)
