# newrelic-xamarin
Xamarin binding for Newrelic mobile agents

Currently iOS bindings work. Android is WIP


Instructions for iOS:

1. There is a Makefile for ios that you can use (make) to build the NewRelicXamarin.iOS.dll that can be included in your Xamarin project. make does:

	a. down a specific version of iOS SDK for New Relic Mobile

	b. unzip the agent zip file and use it to build NewRelicXamarin.iOS.dll

Alternatively, you could use this project inside the Xamarian project and reference it.

2. Makefile uses Microsoft's build tool, msbuild (as xbuild is getting deprecated and replaced by msbuild). You can replace it with xbuild (Xamarin's build tool) if you are on older version of Xamarin.
So if you are still using xbuild, replace
	MONOXBUILD=/Library/Frameworks/Mono.framework/Commands/msbuild
with
	MONOXBUILD=/Library/Frameworks/Mono.framework/Commands/xbuild

3. Add the Newrelic license key in your Xamarin code after you reference this library.

Top of AppDelegate.cs: 

using NewRelicXamarin;


inside the class AppDelegate:

         NRLogger.SetLogLevels((uint)NRLogLevels.All);

         NewRelicXamarin.NewRelic.StartWithApplicationToken("AA75458a1693f5b1cb65232b55ac732d286389bxyz");





Instructions for Android:

TBD
