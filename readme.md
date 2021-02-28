FluentOS GSI PRoject - Android 11.0
===========

This project is based on GSI Project from Phhusson

##How to Build?

To initialize your local repository using the AospExtended trees, use a command like this:

        repo init -u git://github.com/FluentOS-Project/FluentOS-GSI-BlackHole.git -b FluentOS_BlackHole

Sync up the Repo:

        repo sync -c -f -j8 --force-sync --no-clone-bundle --no-tags

Build to your Device:

        . build/envsetup.sh

        lunch treble_arm64_avN-userdebug

        WITHOUT_CHECK_API=true make -j8 systemimage

        xz -c system.img > system.img.xz

        