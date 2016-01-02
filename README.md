# detectdisplays

This is a command-line program to do the equivalent of OS X's Detect Displays (found by holding down option in the Displays preference pane inside System Preferences). It takes no arguments and displays no help—just run it.

## Deprecation

As of this writing (2016-01-02), it now builds on OS X 10.11.12 'El Capitan' but has a deprecation warning going back to 'Mavericks'; I would not expect it to continue working for many revisions in the future.

## Building

To build, open _detectdisplays.xcodeproj_ in XCode, then run Build (⌘B). Assuming no errors, to find the executable, click the disclosure triangle next to _Products_ in the left sidebar, then right- or control-click on _detectdisplays_ and select "Reveal in Finder". Copy the executable to somewhere in your PATH.

## Running as a LaunchAgent

_(Moved from the archived wiki at [Google Code](https://code.google.com/p/detectdisplays/wiki/LaunchAgent).)_

To run this LaunchAgent, place this file at `/Library/LaunchAgents/edu.umich.detectdisplays.plist`.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
        <key>Label</key>
        <string>edu.umich.detectdisplays</string>
        <key>Program</key>
        <string>/usr/local/bin/detectdisplays</string>
        <key>RunAtLoad</key>
        <true/>
        <key>KeepAlive</key>
        <false/>
</dict>
</plist>
```
