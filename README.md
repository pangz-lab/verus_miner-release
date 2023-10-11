
![alt text](https://play-lh.googleusercontent.com/dhd3a8IQFlooE2agHBmyazj49hdV8zNT886J-d99SpQ3gof8I-giyf0AIGoNrSWtrO4p=w240-h480-rw)

# VerusMiner Releases
- VerusMiner is not anymore available for download in playstore due to their new policy against mining apps. Use the following official release site instead.

## Android
<!-- [![name](https://www.gstatic.com/android/market_images/web/play_prism_hlock_2x.png)](https://play.google.com/store/apps/details?id=com.pangzlab.verus_miner&hl=en&gl=US&pli=1) -->
[![name](https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/android-icon.png)](https://pangz-lab.github.io/verusminer/)

## Release Notes
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