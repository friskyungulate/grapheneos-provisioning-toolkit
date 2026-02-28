# GrapheneOS Provisioning Toolkit
This is a toolkit to automate the process of setting up a new GrapheneOS device with sensible defaults and a basic set of apps for activists to use.

## Prerequisites
- A computer running Linux or macOS
    - Windows is not supported at this time. Use a real OS :^)
- [Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools) installed
    - For Linux: [android-udev-rules](https://github.com/M0Rf30/android-udev-rules) installed
- `curl` and `wget` installed

## How to use this toolkit
1. Enable developer options and ADB
2. Plug the phone into your computer and in a shell run `./setup-grapheneos-defaults`
    1. A prompt will appear on the phone asking to trust your computer's ADB fingerprint. Select trust/confirm to continue.
3. Connect to a wifi network.
4. Open Neo Store and grant all permissions it asks for.
5. Enable the FUTO repository in Neo Store's repository settings.
6. Select Signal and FUTO Keyboard in the installed apps view of Neo Store, then manually download and reinstall them
    1. Manually confirm the install/update dialog for each
    2. Doing this seems gratuitous, but is the only way that the installer for each of these apps can be set to Neo Store, which enables unattended updates. Otherwise, the user would have to manually confirm the initial update to each app (which is only needed once), which they may possibly always miss/never do, resulting in updates essentially being blocked for these apps.
7. Install Tor Browser through Neo Store.
5. Open FUTO Keyboard and set it as the default keyboard.
6. Open Settings and delete all saved wifi networks after all the steps above are complete.

## Configurable options
`AUTO_REBOOT_HOURS` is set to 8 and `BLUETOOTH_AUTO_SHUTOFF_MINUTES` is set to 5 in the script. These values were determined by me to be a nice compromise between usability and security. Should your needs be more restrictive or loose than this, edit `setup-grapheneos-defaults` to change these values before running the script.

