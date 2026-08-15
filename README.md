
![alt text](https://play-lh.googleusercontent.com/dhd3a8IQFlooE2agHBmyazj49hdV8zNT886J-d99SpQ3gof8I-giyf0AIGoNrSWtrO4p=w240-h480-rw)

# VerusMiner Releases
- VerusMiner is not anymore available for download in playstore due to their new policy against mining apps. Use the following official release site instead.

## Android
<!-- [![name](https://www.gstatic.com/android/market_images/web/play_prism_hlock_2x.png)](https://play.google.com/store/apps/details?id=com.pangzlab.verus_miner&hl=en&gl=US&pli=1) -->
[![name](https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/android-icon.png)](https://pangz-lab.github.io/verusminer/)

## Release Notes
### v6.0.0
#### 2026/08/09
- ✔️ 37 new CPU-specific optimized miner builds
    - New set of CPU-tuned miner binaries — one optimized build per core type
    - Identified by short tags such as `ca53`, `ca78`, or `kryo`
    - Huge performance improvements compared to previous versions
    - Full list of supported builds: `gen`, `ca34`, `ca35`, `ca53`, `ca55`, `ca57`, `ca65`, `ca65ae`, `ca72`, `ca73`, `ca75`, `ca76`, `ca76ae`, `ca77`, `ca78`, `ca78c`, `ca78ae`, `ca510`, `ca520`, `ca710`, `ca715`, `ca720`, `ca725`, `cr82`, `cx1`, `cx1c`, `cx2`, `cx3`, `cx4`, `cx925`, `nve1`, `nvn1`, `nvn2`, `nvn3`, `nvv1`, `nvv2`, `nvv3`, `thunderx`, `thunderx2t99`, `tsv110`, `apa7`, `apa10`, `apa14`, `apm1`, `ampere1`, `ampere1a`, `a64fx`, `kryo`, `exm3`, `exm4`, `exm5`, `falkor`, `saphira`
    - Unknown CPUs fall back to `gen`

- ✔️ Build recommendation (new)
    - No more guessing which binary fits your phone
    - Open Device Info → Detect CPU topology to get the best recommendation
    - App maps CPU parts to short tags and suggests the best build
    - Compare candidates fairly by running each for a similar duration

- ✔️ Optimized mining (Mining power)
    - **Balanced** — everyday mining with about half your cores
    - **Performance** — prefers faster cores for higher hashrate when plugged in and cooled
    - **Cooler** — fewer cores for cooler operation and longer battery life (great overnight)
    - **Custom** — full manual control of threads and pause limits
    - Comfort pauses: auto-pause on high temperature or low battery, then resume after cooldown

- ✔️ Overnight connection & network tips
    - **Battery unrestricted / don't optimize VerusMiner** — prevents Android from killing the miner
    - **Wi‑Fi stays on when screen is off** — or use solid mobile data
    - Turn off aggressive power saving modes
    - Check OEM battery savers, auto-kill / sleep apps, and game/boost modes
    - Prefer stable 2.4 GHz or wired-router Wi‑Fi near the device
    - Do not swipe VerusMiner away from Recents while mining
    - Use temperature and battery pause limits for clean pauses instead of hard disconnects
    - Tip: plug in for multi-hour runs, pick Cooler or Balanced, and leave space for airflow

- ✔️ History and graphs
    - Session history with ranges (1h to 30d)
    - Live charts while mining: hashrate, temperature, shares, difficulty
    - Last session graphs available even when mining stops
    - History and miner settings saved with complete graphs for performance comparison

- ✔️ Smoother mining UX
    - Clearer home and bottom navigation
    - Easier-to-read metrics (accepted/hour, etc.)
    - Notice if app was force-closed while mining
    - Refreshed onboarding and Quickstart for first-time setup
    - Improved mining screen UI with additional stats (acceptance rate per hour, realtime pool accepted hashrate)
    - Warning added for using default Verus Coin Foundation wallet address

- ✔️ Custom Mining Pool / Stratum
    - Creation of custom stratum is now supported
    - Add custom stratum pool that appears in stratum selection when creating miner setting

- ✔️ Look and language
    - Multiple themes (including community styles)
    - More languages via refreshable language packs

- ✔️ Speed test and Network debug
    - Refined speed test feature — fastest pinged pool goes to the top first
    - Network debug feature added to check network status during mining

- ✔️ VerusBox Compatibility
    - Still compatible, especially local monitoring and remote control feature
    - New VerusBox version release coming soon

- ✔️ Online Monitoring is back
    - MyVerusMiners — successor of VersuMonitor web app
    - Automatically connects to MyVerusMiners to view miners while away
    - Access at https://my-verusminers.pangz.space/ or from the app
    - Always free to use

- ✔️ Tips after updating
    - Open Device Info → detect CPU topology (stop mining first)
    - Install suggested short-tag build (e.g. `ca78`) from GitHub if upgrade recommended
    - Try Mining power: Balanced daily, Performance when plugged in, Cooler overnight
    - Open Keep mining connected and finish battery + Wi‑Fi items for each phone
    - Refresh languages/themes for latest remote packs
### v5.0.0
#### 2024/02/05
- ✔️ New features
	- added onboarding
	- added quickstart guide
	- added a guide page where you can find helpful videos and blogs
- ✔️ Better support for foreground process
	- miner can now run with screen off
	- added mining status in device notification
- ✔️ Miner improvements
	- expect an improved hashrate on some old phone models
- ✔️ UI fix and improvements
	- redesigned the miner setting list view screen
	- improved setting info in mining base screen
	- updated the messages and layout for home screen
- ✔️ Added update notifier
	- when a new version is released, a new page will popup.
- ✔️ Improved speed test feature UI and behavior
- ✔️ Added duplicate, set default and qr feature in setting list view
- ✔️ Updated paddypool mining servers
- ✔️ Updated web links

### v4.2.0
#### 2023/10/12
- ✔️ UI improvements
	- updated monitoring icons from the miner main screen
	- added online monitoring link in the main miner view
- ✔️ Added monitoring selection dialog for setting up the monitoring
- ✔️ Enabled online monitoring by default
- ✔️ Added support for other CPU models
	- `txt81`  -> thunderxt81
	- `txt88`  -> thunderxt88
	- `txt83`  -> thunderxt83
	- `tx2t99` -> thunderx2t99

### v4.0.1
#### 2023/10/09
- ✔️ Added support for online monitoring - official site https://verusmonitor.is-now.live/
- ✔️ Added new mining pools
- ✔️ Built with more optimized miner by adding a support for specific CPU models
	- `gen`  -> generic
	- `ca35` -> cortex-a35
	- `ca53` -> cortex-a53
	- `ca55` -> cortex-a55
	- `ca57` -> cortex-a57
	- `ca72` -> cortex-a72
	- `ca73` -> cortex-a73
	- `ca75` -> cortex-a75
	- `exm1` -> exynos-m1
	- `flkr` -> falkor
	- `saphira` -> saphira
	- `tx`		-> thunderx

### v3.4.1
#### 2023/06/28
- ✔️ Fixed setting compatibility(from version 3.3.0)

### v3.4.0
#### 2023/06/26
- ✔️ Improved speed test feature
	- added retry button for failed connection test
- ✔️ Added temperature control setting
- ✔️ Added charge control setting

### v3.3.0
#### 2023/06/11
- ✔️ Added speed test feature
	- mining pool connection speed can now be tested
	- this is an experimental feature so some issues can be expected
- ✔️ Mining improvements
	- miner binary update with hashing optimization
- ✔️ Minor UI improvements
	- app and miner version is added at the main mining screen
- ✔️ Bug fix
	- pool drop-down default value is set correctly when scanning a setting

### v3.2.0
#### 2023/06/07
- ✔️ Mining improvements
	- enabled extra-nonce(xnsub) by default
	- better mining support for nicehash pool

### v3.1.0
#### 2023/06/05
- ✔️ Mining view improvements
	- center mining detail view
- ✔️ Secured monitoring connection - now using TLS/SSL certificates
- ✔️ Monitoring server re-connection improvements
	- improved status send timing(requires VerusBox v3.1.0)

### v3.0.0
#### 2023/06/04
- ✔️ Upgraded the Verus coin miner
	- Now supports the latest features of Verus - PBaaS and merge mining
- ✔️ Improved mining performance
- ✔️ Mining view improvements
	- updated miner screen layout
	- stop button now becomes a slider
	- re-positioned, restyled and resized UI elements
	- added confirmation before exiting the mining screen
- ✔️ Minor UI improvements
- ✔️ Added wallet balance view
- ✔️ Added new mining pools
- ✔️ Monitoring server reconnection improvements

### v2.2.0
#### 2023/01/21
- ✔️ Custom non-Verus wallet address can now be used
- ✔️ Existing flags can now be overriden by the custom parameters field
- ✔️ Fixed welcome add setting button stack position
- ✔️ Added long polling feature
- ✔️ Enable the stratum server and port for custom input
- ✔️ Updated input text field property
- ✔️ Show [ CUSTOM ] for custom wallet address or stratum server
- ✔️ Minor UI changed for the miner setting main screen

### v2.1.1-rc1
#### 2022/12/05
- ✔️ Improved miner setting
	- support for custom wallet address
	- better support for custom parameters
- ✔️ Improved monitoring server reconnection
- ✔️ Minor UI improvements