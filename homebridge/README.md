# Homebridge Add-On For Home Assistant

This is a [Homebridge](https://homebridge.io) add-on for [Home Assistant](https://www.home-assistant.io). Homebridge provides a lightweight HomeKit API implementation with plugin support.

Unlike the [original](https://github.com/davide125/hassio-addons/tree/main/homebridge), this version will always try to use the latest docker image to ensure Homebridge is always updated. This could cause unintended behaviour, so be sure this is really what you want. 

This will not be a good solution for people using older plugins that are not compatible with the latest Homebridge version (2.x as of today).


Note that Home Assistant supports HomeKit natively these days, both as a [controller](https://www.home-assistant.io/integrations/homekit_controller/) and as a [device](https://www.home-assistant.io/integrations/homekit/), so you probably don't need Homebridge if you just want to integrate with the HomeKit ecosystem. However, Homebrige has a lot of plugins, so it can still be useful to bridge some less-supported devices (e.g. [Nest](https://github.com/chrisjshull/homebridge-nest)) into Home Assistant.

## Installation
1. Add the [add-on repository](https://github.com/iSteve-O/hassio-addons) in Home Assistant.

    *If moving from an old HB add-on, remove it first.
2. Install Homebridge from the add-on store once visible.

    *If previously using another HB add-on, you may have to delete its repo also.
4. Tap START to begin running the add-on. (See below if restoring from backup)

    <b>*If restoring from a backup, stop the old instance first for the best chance of a successful restore.</b> (see below)
5. Tap OPEN WEBUI to configure your new instance.

## Configuration
To configure Homebridge click on OPEN WEB UI from the add-on page.

## Restoring From A Backup
If moving from another Homebridge instance, you should first make sure the old one is fully updated (all plugins, node.js, etc., even if updates are not persistent). 

1. Create & save a backup of the fully updated old Homebridge instance in settings.
2. Shut down the old instance
3. Start the new instance by tapping START on the add-on.
4. Tap OPEN WEB UI in the add-on to configure the new instance
5. Restore your backup in the Homebridge web UI.

If your old Homebridge instance is not fully up to date, restoring the backup could cause unforeseen issues since this add-on will be fully updated.


## Credits
This add-on and its repo were forked from [Davide125](https://github.com/davide125/hassio-addons) so I could try to update the docker image more often. This add-on uses the latest image of [Docker Homebridge](https://github.com/homebridge/docker-homebridge) directly from its source. The add-on icon is from [Homebridge](https://github.com/homebridge/homebridge).
