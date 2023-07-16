Based on [this Reddit post](https://www.reddit.com/r/AndroidQuestions/comments/pzayw9/extracting_ringtonealarm_sounds_from_galaxy_s9/)

# android_sound_extraction_instructions.md

1. Download [Platform Tools](https://developer.android.com/studio/releases/platform-tools) from the official Android developer website.

2. Open PowerShell and navigate to the downloaded `platform-tools` directory using the following commands:
   ```powershell
   cd .\Downloads\platform-tools_r34.0.4-windows\platform-tools\
   ```

3. Connect your Galaxy S9 device to your computer using a USB cable.

4. In PowerShell, run the following command to check if your device is detected:
   ```powershell
   ./adb devices
   ```

5. To extract the notification sounds, run the following command:
   ```powershell
   ./adb shell ls /system/media/audio/notifications/
   ./adb pull /system/media/audio/notifications/ ./Extracted
   ```

6. To extract the ringtones, run the following command:
   ```powershell
   ./adb shell ls /system/media/audio/ringtones/
   ./adb pull /system/media/audio/ringtones/ ./Extracted
   ```

7. To extract the UI sounds, run the following command:
   ```powershell
   ./adb shell ls /system/media/audio/ui/
   ./adb pull /system/media/audio/ui/ ./Extracted
   ```
