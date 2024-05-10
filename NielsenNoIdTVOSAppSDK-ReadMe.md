Nielsen No Id TVOS App SDK Release Notes
For integration help, visit https://engineeringportal.nielsen.com/docs/DCR_&_DTVR

Release 9.3.0.0 (5-10-2024) 
- Support for privacy manifest with tracking domain for Ad flavors.
- Support for capturing user opt-out during initialization.
- Other bug fixes and enhancements. 

Release 9.2.0.0 (9-27-2023) 
- Support for privacy manifest and required reason API introduced in XCode 15.
- Digitally signed SDK framework per Apple recommendation.
- DCR Static recognizing metadata with changed assetID for new impressions. 
- Limiting ping retries during https failures. 
- Other bug fixes and enhancements. 

Release 9.1.0.0 (03-31-2023)
- DCR Static duration measurement for individual page section/assets.
- Removed use of iOS keychains, replaced with NSUserDefaults for persistent storage.
- Support to enable Viewability feature by product (DCR, DTVR).
- Other bug fixes and enhancements.

Release 9.0.0.0 (10-07-2022)
- Viewability measurement for DTVR, DCR Content and DCR Ad products. 
- Audibility measurement for DTVR, DCR Content and DCR Ad products.
- SDK built with Xcode 14.
- Other bug fixes and enhancements.

Release 8.2.0.0 (3-21-2022)
- Adopting Swift language internally, built on mixed model (Swift+Objective C).
- Support for Swift markers to help Swift developers.
- Removed the usage of deprecated iOS network reachability class.
- Disabled iCloud backup/synchronization of SDK keychain items.
- Other bug fixes and enhancements.

Note: If you experience build errors while using static framework, please follow the instructions: https://engineeringportal.nielsen.com/docs/iOS_Static_Framework_Setup

Release 8.1.0.0 (6-28-2021)
- Support for XCFramework build distribution.
- Support for MacOS Catalyst platform framework.
- Fixed the device classification for MacOS M1 measurement.
- Support to capture Hashed email and UID.
- Support to collect SDK diagnostic data.
- Other bug fixes and enhancements.

Release 8.0.0.0 (10-05-2020)
- iOS 14 App Transparency Framework support.
- FPID and VendorID support.
- Fixed the device classification for iPADOS measurement.
- Support for Android apps running on ChromeOS.
- Support for Xamarin cross platform framework.
- Other bug fixes and enhancements.

Release 7.2.0.0 (5-18-2020)
- DTVR AQH and IVD requirements for End and pause timeout
- Support for Hybrid app webview measurement
- Support for Hybrid app react native webview measurement
- Support for react native measurement
- Other Bug Fixes and Enhancements.

Release 7.1.0.0 (12-9-2019)
- Removed usage of deprecated class UIWebView 
- Offline viewing measurement enhancements 
- Fixed deadlock on SDK shutdown 
- Revisited precedence logic for sfcode parameter
- Fix for DCR individual ad pings parameters after channel change 
- Using default value for incorrect adModel parameter
- Defaulting isLive parameter value on channel change 
- Other fixes and enhancements.

Release 7.0.0.0 (9-6-2019)
- Support for CDN based config.
- Support for Market based EMM UAID pings.
- Changes required for proper DCR Static measurement in multi-instance/multiple appid's case.
- Fixes for OTT synchronization issues between iOS and Android platforms.
- Fixes for EV data parameters in few scenarios.
- Fixes for DCR Static product behaviour in background app refresh and background fetch scenarios.
- DCR Ad reporting improvements.
- Fixes and improvements for the SDK console log messages.
- Other enhancements and fixes.
s
Release 6.2.0.0 (2-4-2019)
- Location measurement has been removed from the SDK code.
- Location frameworks were there previously but disabled, now it’s fully removed to avoid confusion from noticing it being included at all. Code was there because SDK used to collect. Then the function was disabled. Even having it there, clients used to be like "why are you having that framework there?" It raised privacy/security concerns and suspicion.
- Increased SDK log file size from 2mb limit to 50mb for Debug mode. Logs will not rollover so quickly so that longer debug sessions can be analyzed.
- Removed OTT Airplay/mirroring detection that caused crashes in AVAudioSession class.
- DCR performance improvements.
- Fixed the parsing error happening when clientid/vcid provided as empty in metadata. In case where clientid/vcid is not supplied, SDK will take default from config instead of using the blank value.
- Implemented buildversion naming convention. Help monitor SDK flavor (artifactory/Adobe Launch/standalone/etc) and market (AGF/Global).
- Align AppSDK for FW detection with BSDK where for DCR use a variable nol_cmsIntrvlGp (value is 2) rather than nol_id3IntrvlGp(15). Detect forward event with >2 seconds of scrub for DCR instead of 15 seconds as currently. This may result in more FW events in EVdata as well as less duration.
- Other Bug Fixes/Enhancements.
