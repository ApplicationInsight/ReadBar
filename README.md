# ReadBar
A very basic barcode reader for use when the user needs to check when two or more barcodes match.

In many circumstances it is important to check that a number of objects are all members of the same set. If the objects are labelled with barcodes, a user can read the barcodes and confirm they are all the same. This app enables users to read a number of one-D barcodes (the default type it reads is org.iso.Code39), and either confirms they are all identical, or warns the user that they are not.

The iOS prototype app was created at the January 2017 NHS HackDay at Cardiff in response to a pitch given by Martyn Read.

Martyn Read and Dave Kilroy collaborated on the project using LiveCode (www.livecode.com & www.livecode.org). More polish will follow, as will an Android version.

What exists here currently is where the app got to as at 2:30pm on the afternoon of Sunday 29th January.

Everything is inside the 'the-app' folder:

- folder: the-app

    -   REadBar004013.livecode

        -   this is a LiveCode stackfile, to open it you need to get the LiveCode IDE from their website (to get the community version which is free go to the .org as opposed to the .com website)

        -   stackfiles are binary files containing both code and the gui - as such I'm not trying to use git version control (although there are avenues to this with LiveCode - but that is a discussion for another day)

        -   the numbering I'm using shows that this is version 004 of the app (take it as shorthand for version 0.0.4), and my 'stacknumber' for this livecode file is 013

- folder: stack-archive

    -   these contain all the older versions of stackfiles - as I can't use git version control (see above) I do regular saves agains imcrementing file names
    

- folder: audio

    -   this folder contains the three audio files I use to indicate:

        -   a barcode read which matches the previous reading (or the first barcode reading in a series)

        -   a bad match reading where the current reading did not match the previous reading

        -   a final reading in a series where all the barcode readings matched - i.e. a successful series of readings

- folder: builds

    -   folder: 004

        -   build files for this version of the app

        -   currently only contains a folder for iOS builds (future versions will also contain Android builds)

        -   folder: iOS

            -   contains the 3 files needed to install on an iOS device from a remote URL (beta.html, manifest.plist, ReadBar.ipa)

            -   please note that as an app in beta - i.e. as an app running with a 'developer' provisioning profile from Apple, it will only install on iOS devices that have their UDIDs included in the provisioning profile. If you wish to test this app on your device using my (Dave Kilroy's) Apple certification then please send my your device's UDID

- folder: images-non-app

    -   contains the icon image (created by Martyn Read) in the various sizes needed for iOS and Android phones

    -   Note: I have not yet included them in the build...

The actual barcode reading is done by using the mergAV LiveCode external (currently to access this you will need an 'Indy' licence from LiveCode - until they finish their 'LiveCode Infinity' project).

Please get in touch if you want information on LiveCode or what I've done so far.
