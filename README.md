GoogleAnalytics
=====
This is the Google Analytics module for Godot Engine (https://github.com/okamstudio/godot)
- Android only
- Register Screens
- Register Events

How to use
----------
Drop the "analytics" directory inside the "modules" directory on the Godot source.

Recompile.

In Example project goto Export->Target->Android:

	Options:
		Custom Package:
			- place your apk from build
		Permissions on:
			- Access Network State
			- Internet

Configuring your game
---------------------

To enable the module on Android, add the path to the module to the "modules" property on the [android] section of your engine.cfg file. It should look like this:

	[android]
	modules="org/godotengine/godot/GodotGoogleAnalytics"

If you have more separete by comma.

API Reference
-------------

The following methods are available:
```python

# Change Dispatch Period
# @param int dispatch_period The dispatch period (default: 1800)
setDispatchPeriod(dispatch_period)

# Change Sample Rate
# @param double sample_rate The sample frequency in percentage (default: 100.0d)
setSampleRate(sample_rate)

# Change Anonymize IP
# @param boolean anonymize_ip Option to hide or not the IPs of the users (default: false)
setAnonymizeIp(anonymize_ip)

# Change AdIdCollection
# @param boolean ad_id_collection Option for monitorize Ads (default: true)
setAdIdCollection(ad_id_collection)

# Change Dry Run
# @param boolean dry_run Option for dry run (default: false)
setDryRun(dry_run)

# Init GoogleAnalytics (change the previous params before init)
# @param string tracker_id The tracker ID (UA-XXXXXXX-X)
# @param string app_version The version of the game (0.1.2)
# @param string app_name The name of the game (My Game)
# @param string bundle_id The package id (com.company.game)
init(tracker_id, app_version, app_name, bundle_id)

# Register screen
# @param string name The name of the screen
screen(name)

# Register event
# @param string category Category of the event
# @param string action Action of the event
event(category, action)
```

References
-------------
Google Analytics Services:
* https://developers.google.com/android/reference/com/google/android/gms/analytics/GoogleAnalytics
* https://developers.google.com/analytics/devguides/collection/android/v4/?hl=es


License
-------------
MIT license
