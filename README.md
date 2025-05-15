# PerfDoze

PerfDoze is a powerful performance optimization tool for rooted Android devices that allows users to fine-tune system resources for individual applications.

## 📸 Screenshots

<div style="display: flex; flex-wrap: wrap; justify-content: space-around; gap: 10px;">
  <img src="https://raw.githubusercontent.com/abhijitpatle/perfdoze/main/screenshot1.jpg" width="45%" />
  <img src="https://raw.githubusercontent.com/abhijitpatle/perfdoze/main/screenshot2.jpg" width="45%" />
</div>



## Features

- **Per-App Performance Profiles**: Configure different performance modes for each app based on your needs
- **Real-Time Monitoring**: Track CPU usage, GPU utilization, and RAM consumption for configured apps
- **Root-Level Optimizations**: Utilize root access to make system-level performance adjustments
- **Automatic Mode Switching**: Background service detects when apps are launched and applies the appropriate performance profile
- **Smooth UI**: Modern, responsive interface with Material Design elements for a great user experience

## Performance Modes

### Gaming Mode 🎮
- Maximizes CPU & GPU performance to highest settings
- Disables thermal throttling where possible
- Kills background processes to free up RAM
- Force stops non-gaming apps to allocate more resources
- Sets highest priority for the game app
- Prevents Android from killing the game

### Performance Mode ⚡
- Balances speed and efficiency
- Sets CPU to performance governor
- Enables GPU boost without extreme settings
- Prioritizes the app without closing others
- Great for productivity apps and media streaming

### Default Mode 🔄
- Returns app to system default settings
- Normal CPU governor (usually schedutil)
- Standard GPU settings
- Default app priority and background behavior
- Balanced for everyday use

### Battery Save Mode 🔋
- Reduces power consumption
- Sets CPU to powersave governor
- Lowers maximum CPU frequency
- Disables GPU boost features
- Restricts background operations
- Automatically force-stops app when inactive for 60+ seconds

## How It Works

PerfDoze utilizes several advanced Android system features to optimize performance:

1. **Root Access**: Uses privileged commands to modify system settings that are normally inaccessible
2. **CPU Governor Control**: Directly writes to `/sys/devices/system/cpu/*/cpufreq/scaling_governor` to control CPU behavior
3. **GPU Frequency Management**: Interfaces with GPU settings through `/sys/class/kgsl/kgsl-3d0/` to manage graphics performance
4. **App Priority Management**: Uses Android's app standby buckets and background processing flags
5. **Accessibility Service**: Monitors app switches to automatically apply performance modes
6. **Native Integration**: Uses Flutter Method Channels to communicate with native Kotlin code for system-level access

## Technical Details

- **CPU Optimization**: PerfDoze can modify CPU governor settings (performance, powersave, schedutil), adjust minimum and maximum frequencies, and manage core usage
- **GPU Optimization**: Controls GPU clock speeds, bus frequencies, and thermal throttling settings
- **Memory Management**: Can terminate background processes to free up RAM for foreground applications
- **App Priority Control**: Manipulates Android's built-in app standby buckets and background processing flags
- **Thermal Management**: Can temporarily disable or modify thermal throttling behavior (use with caution!)

## Requirements

- Rooted Android device (SuperSU, Magisk, or similar root management tool)
- Android 8.0 (API level 26) or higher
- Usage Stats permission
- Accessibility Services permission (optional, for automatic mode switching)

## Getting Started

1. Install PerfDoze on your rooted Android device
2. Launch the app and grant root access when prompted
3. Allow Usage Stats permission from the permission screen
4. Enable Accessibility Service for automatic mode switching (optional)
5. Browse your installed apps in the "All Apps" tab
6. Tap on any app to configure a performance mode
7. Configured apps will appear in the "Configured Apps" tab with performance metrics

## Usage Tips

- **Gaming Mode**: Use for graphics-intensive games that need maximum performance
- **Performance Mode**: Good for productivity apps, video streaming, or moderate gaming
- **Default Mode**: Ideal for everyday apps where balanced performance is sufficient
- **Battery Save Mode**: Best for non-critical apps when battery life is a priority
- **Monitor Metrics**: Check the Configured Apps tab to see real-time performance data
- **App Conflicts**: If multiple gaming apps are configured, they won't force-stop each other

## Warning

PerfDoze modifies system-level settings that can potentially:
- Increase battery consumption
- Cause thermal throttling or overheating on some devices
- Affect overall system performance
- Reduce device lifespan if used improperly

Use with caution, especially Gaming Mode and settings that disable thermal management.

## License

This application is provided as-is under the MIT License. See LICENSE file for details.

## Credits

Developed by Abhijeet. Icons and design elements created for PerfDoze.
@abhijitpatle @perfdoze , #AbhijitPatle #perfdoze
