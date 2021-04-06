FluentOS GSI PRoject - Android 11.0
===========

This project is based on GSI Project from Phhusson

##How to Build?

To initialize your local repository using the AospExtended trees, use a command like this:

        repo init -u git://github.com/FluentOS-Project/manifest.git -b a11

Sync up the Repo:

        repo sync -c -f -j8 --force-sync --no-clone-bundle --no-tags

Build to your Device:

        . build/envsetup.sh
        
        Build A Only Vanilla No SuperSU:
        lunch treble_arm64_avN-userdebug

        Build A/B Vanilla No SuperSU:
        lunch treble_arm64_bvN-userdebug

        Build A Only Gapps with SuperSU:
        lunch treble_arm64_agS-userdebug

        Build A/B Gapps with SuperSU:
        lunch treble_arm64_bgS-userdebug

        Build A Only Gapps No SuperSU:
        lunch treble_arm64_agN-userdebug

        Build A/B Gapps No SuperSU:
        lunch treble_arm64_bgN-userdebug

        WITHOUT_CHECK_API=true make -j8 systemimage

        Go to out/target/product/phh_*/ and use this code:
        xz -c system.img > system.img.xz

        
