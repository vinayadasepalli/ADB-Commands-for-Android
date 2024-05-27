# Introduction to ADB
Android Debug Bridge (ADB) is a versatile command-line tool that allows you to communicate with an Android device from your computer. It provides a bridge for developers to debug their applications, but it's also a powerful tool for Android enthusiasts to perform various tasks on their devices.

## Basic ADB Commands
### ADB Server
adb kill-server: Stops the ADB server running on your computer.  
adb start-server: Starts the ADB server if it's not already running.

### ADB Reboot
adb reboot: Reboots the device normally.  
adb reboot recovery: Reboots the device into recovery mode.  
adb reboot-bootloader: Reboots the device into bootloader or fastboot mode.  
adb root: Restarts ADB with root permissions, if available.  

### Shell
adb shell: Opens an interactive shell on the device, allowing you to run commands directly.  

### Devices
adb devices: Lists all devices connected to the computer.  
adb connect [ip_address_of_device]: Connects to a device over TCP/IP.  
adb usb: Connects to a device via USB.  

### Get Device Android Version
adb shell getprop ro.build.version.release: Retrieves the Android version installed on the device.  

### LogCat
adb logcat: Displays real-time system logs from the device.  
adb logcat -c: Clears the current logs on the device.  
adb logcat -d > [path_to_file]: Saves the logcat output to a file on the local system.  
adb bugreport > [path_to_file]: Generates a bug report including device information, system logs, and more.  


## Managing Apps
### App Install
adb install [path/to/app.apk]: Installs an app on the device.  
adb uninstall [package_name]: Uninstalls an app from the device.  
adb shell pm clear [package_name]: Clears all data associated with a package.  

### App Update
adb install -r [path/to/app.apk]: Reinstalls an app and keeps its data intact.  
adb install –k [path/to/app.apk]: Installs an app with forward lock (previously installed on a different device).  

### App Interaction
adb shell am start [options]: Starts an activity specified by the intent options.  
adb shell am broadcast [options]: Sends a broadcast to all interested broadcast receivers.  



## Device Information and Settings
### Battery and Power
adb shell dumpsys battery: Retrieves battery status information.  
adb shell dumpsys battery set level [n]: Sets the battery level to a specified value.  

### Screen and Display
adb shell wm size [WxH]: Sets the screen resolution to the specified width and height.  
adb shell wm density [density]: Sets the screen density to the specified value.  

### System Information
adb shell get-state: Prints the current state of the device.  
adb shell get-serialno: Prints the serial number of the device.  
adb shell dumpsys: Dumps system service information.  
