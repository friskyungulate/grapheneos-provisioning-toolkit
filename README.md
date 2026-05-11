# GrapheneOS Provisioning Toolkit
This is a toolkit to automate the process of setting up a new GrapheneOS device with sensible defaults and a basic set of apps for activists to use.

## Prerequisites
- A computer running Linux or macOS
    - Windows is not supported at this time. Use a real OS :^)
- [Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools) installed
    - For Linux: [android-udev-rules](https://github.com/M0Rf30/android-udev-rules) installed
- `jq` and `curl` installed

## How to use this toolkit
1. Enable developer options and ADB
2. Plug the phone into your computer and in a shell run `./setup-grapheneos-defaults`
    1. A prompt will appear on the phone asking to trust your computer's ADB fingerprint. Select trust/confirm to continue.
3. Connect to a wifi network.
4. Open Neo Store, enable the FUTO F-Droid Repository in Neo Store's repository settings, then select "Sync & Start". Open FUTO Keyboard and set it as the default keyboard.
5. Open Settings and delete all saved WiFi networks after all the steps above are complete.

## Configurable options
`AUTO_REBOOT_HOURS` is set to 8 and `BLUETOOTH_AUTO_SHUTOFF_MINUTES` is set to 5 in the script. These values were determined by me to be a nice compromise between usability and security. Should your needs be more restrictive or loose than this, edit `setup-grapheneos-defaults` to change these values before running the script.

