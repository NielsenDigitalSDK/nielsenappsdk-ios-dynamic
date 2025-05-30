VRI App SDK Release Notes  
For integration help, visit https://engineeringportal.nielsen.com/docs/DCR_&_DTVR

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
