Using with InteliJ IDEA
=======================

Workarounds
-----------

IDEA does not properly import Eclipse projects:

* Resources are overwriten, so `pref_entryValues_cameraResolution` and similar resources could not be found. So `res` folder must be copied after import to fix this.
* To import `ARBaseLib` as module you need to open it with IDEA first.
* Project dependences are not recognised. You need to manually `Project Settings`->`Modules`->`Add`->`New module`. `ARBaseLib` must be added as a dependency module to your example projects. While importing, use package name `org.artoolkit.ar.base`, so `gen` folder will be correct.
* Remove `com.android.ide.eclipse.adt.DEPENDENCIES` as you are adding `ARBaseLib` manually. `Add`->`Module Dependency`
* In `Project Settings`->`Project` ensure, that `Project SDK` is Android not Java deskop.
* When running, `Target device` should be `USB device`. Examples will not work with emulatror.

Usage
-----

Launch default Activity.
Open in computer or print marker from `../doc/patterns/Hiro pattern.pdf` folder.
Examples will draw 3D cube, when marker is recognised in Android Camera view.