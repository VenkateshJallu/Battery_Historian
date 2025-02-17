# Battery Historian

Battery Historian is a tool that processes Android bug reports and visualizes various power-related information, helping developers and users diagnose battery-draining issues on Android devices.

## Table of Contents
1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Usage](#usage)
4. [Understanding the Output](#understanding-the-output)
5. [Key Tags and Their Importance](#key-tags-and-their-importance)
6. [FAQ](#faq)
7. [Contributing](#contributing)
8. [License](#license)

## Introduction

Battery Historian is designed to help developers and users understand the battery usage patterns of their Android devices by analyzing bug reports. It provides a visual representation of various power-related events and metrics, making it easier to identify and diagnose issues that lead to battery drain.

## Getting Started

### Prerequisites

- A computer with Python installed.
- An Android device.
- A bug report generated from the Android device.

### Installation

1. Clone the Battery Historian repository:

   ```bash
   git clone https://github.com/google/battery-historian.git
   cd battery-historian
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Generating a Bug Report

1. Connect your Android device to your computer via USB.
2. Enable Developer Options and USB Debugging on your device.
3. Run the following command to generate a bug report:

   ```bash
   adb bugreport bugreport.zip
   ```

4. Extract the bug report:

   ```bash
   unzip bugreport.zip -d bugreport
   ```

## Usage

1. Run Battery Historian:

   ```bash
   python historian.py --report bugreport/bugreport.txt
   ```

2. Open the generated HTML report in your web browser to view the visual representation of the battery usage data.

## Understanding the Output

The Battery Historian output is divided into several sections, each representing different aspects of battery usage. Here are some key sections to focus on:

### Battery Level

Displays the battery charge level over time. Sudden drops or abnormal consumption patterns can indicate issues.

### Screen On/Off

Shows when the device screen is turned on or off. Frequent or prolonged screen-on times can significantly impact battery life.

### CPU Usage

Displays the CPU usage by various processes. High CPU usage can lead to faster battery drain.

### Wake Locks

Shows wake locks held by apps or services. Wake locks prevent the device from entering deep sleep, leading to battery drain.

### Network Connectivity

Displays changes in network connectivity (Wi-Fi, mobile data). Network activities can drain the battery.

### GPS Usage

Shows when GPS is being used by apps. Frequent or prolonged use can significantly impact battery life.

### Power-Consuming Apps

Lists apps that consume a significant amount of power. Identifying these apps helps in diagnosing and optimizing battery usage.

## Key Tags and Their Importance

Battery Historian is a tool that processes Android bug reports and visualizes various power-related information. It helps diagnose battery-draining issues by highlighting key events and metrics. Below are the key tags used in Battery Historian, their usage, and their importance:

## 1. Battery Level
**Tag:** `BatteryLevel`
- **Usage:** Displays the battery charge level over time.
- **Importance:** Helps identify periods of high battery drain and correlate them with other events or processes.

## 2. Screen On/Off
**Tag:** `ScreenOn`
- **Usage:** Indicates when the device screen is turned on or off.
- **Importance:** Screens consume significant power. Frequent or prolonged screen-on times can impact battery life.

## 3. CPU Usage
**Tag:** `CpuUsage`
- **Usage:** Shows the CPU usage by various processes.
- **Importance:** High CPU usage can lead to faster battery drain. Identifying apps with excessive CPU consumption is crucial for optimization.

## 4. Wake Locks
**Tag:** `WakeLock`
- **Usage:** Displays information about wake locks held by apps or services.
- **Importance:** Wake locks prevent the device from entering deep sleep, leading to battery drain. Identifying and managing wake locks is essential for power optimization.

## 5. Network Connectivity
**Tag:** `Connectivity`
- **Usage:** Shows changes in network connectivity (Wi-Fi, mobile data).
- **Importance:** Network activities, especially frequent changes or high data usage, can drain the battery.

## 6. GPS Usage
**Tag:** `GpsUsage`
- **Usage:** Indicates when GPS is being used by apps.
- **Importance:** GPS is a power-hungry component. Frequent or prolonged use can significantly impact battery life.

## 7. Power-Consuming Apps
**Tag:** `PowerUse`
- **Usage:** Lists apps that consume a significant amount of power.
- **Importance:** Identifying power-hungry apps helps in diagnosing and optimizing battery usage.

## 8. Kernel Wakelocks
**Tag:** `KernelWakelock`
- **Usage:** Displays kernel-level wakelocks that keep the device awake.
- **Importance:** Kernel wakelocks can prevent the device from sleeping, leading to power drain.

## 9. Temperature
**Tag:** `BatteryTemperature`
- **Usage:** Shows the temperature of the battery over time.
- **Importance:** High temperatures can indicate heavy usage or potential issues with the battery or device.

## 10. Charging and Discharging Cycles
**Tag:** `ChargeCycle`
- **Usage:** Indicates periods of charging and discharging.
- **Importance:** Helps in understanding charging patterns and identifying any irregularities.

## 11. App Usage
**Tag:** `AppUsage`
- **Usage:** Displays usage patterns of various apps.
- **Importance:** Background activities of apps can lead to unnoticed battery drain.

## 12. Event Timelines
**Tag:** `Event`
- **Usage:** Correlates various events (e.g., connectivity changes, screen state) with battery level changes.
- **Importance:** Understanding event timelines helps in diagnosing the root causes of battery drain.

## 13. Battery Drain Rate
**Tag:** `DrainRate`
- **Usage:** Shows the rate at which the battery is draining.
- **Importance:** Identifying periods of high drain rate helps in pinpointing resource-intensive activities or issues.

## 14. Partial Wakelocks
**Tag:** `PartialWakelock`
- **Usage:** Displays partial wakelocks held by apps or services.
- **Importance:** Partial wakelocks keep the CPU awake but allow the screen to be off. Managing these can help in reducing battery drain.

## 15. Top Apps
**Tag:** `TopApp`
- **Usage:** Lists the top apps consuming battery power.
- **Importance:** Identifying top battery consumers aids in optimizing app usage and improving battery life.

By focusing on these tags and understanding their implications, you can effectively diagnose and address battery-related issues in Android devices using Battery Historian.

## FAQ

### How can I generate a bug report?

Follow the steps in the "Generating a Bug Report" section to generate and extract a bug report from your Android device.

### How do I interpret the Battery Historian output?

Refer to the "Understanding the Output" section for detailed explanations of each section in the Battery Historian report.

### How can I identify battery-draining apps?

Check the "Power-Consuming Apps" section in the Battery Historian report to identify apps that are consuming a significant amount of power.

## Contributing

We welcome contributions to Battery Historian. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with a clear message.
4. Push your changes to your forked repository.
5. Create a pull request to the main repository.

Please ensure your code adheres to the project's coding standards and includes appropriate tests.

## License

Battery Historian is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for more information.
