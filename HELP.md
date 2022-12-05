# HOW TOs :
## Setup Monitoring Server using VerusBox

### 📝Note
- VerusBox monitoring service works in combination with the VerusMiner app
- Each app should be installed in a separate devices to work
- VerusMiner is more stable and optimized than the VerusBox's mining version
- Monitoring is designed to work in a check-it-when-you-need-it basis so it doesn't have to be up all the time
- You may use a dedicated phone or tablet but it's not required
- Monitoring works within your local network

### Requirements

#### 📲 Download the following apps
1. [VerusBox](https://play.google.com/store/apps/details?id=com.pangzlab.verus_box&gl=US)
2. [VerusMiner](https://play.google.com/store/apps/details?id=com.pangzlab.verus_miner&gl=US)

### 🥓 Part 1 of 2 [ VerusBox Installation ]
1. Install `VerusBox`
2. Open VerusBox then go to `Tools` > `Monitoring`
3. Go to setting ⚙️ and setup the `IP ADDRESS` and `PORT` then save
    - make sure you are connected to your Wifi.
    - the IP address should be the same as the IP address of your device connected to the network
    - it is recommended to set the IP address as a static IP to avoid changing all client settings when your local network changes (see [Qs](#questions))
4. If everything is setup correctly, no error message should appear
5. An error will appear if the `IP address you set and your device's IP is different`.
    - check your connection setting and get the current IP and use it
    - `PORT` number can be anything. You can leave it as it is
6. From the `Monitoring` main screen, find the slider. `Slide it to start the server`.
7. Leave it open to wait for any incoming connections


### 🧀 Part 2 of 2 [ VerusMiner Installation ]
1. Install `VerusMiner`
2. Open VerusMiner and go to `More` > `Monitoring` then add by clicking `+` (plus sign) at the bottom
3. Add a setting by using the `IP ADDRESS` and `PORT` number you set from the `VerusBox`
    - the IP ADDRESS and PORT number should be the same as the one you used in VerusBox
    - save it or check the connection by pressing the `CHECK CONNECTION` button.
    - a popup message should appear with a success message when the connection is established
4. Go to `More` > `Setting` > `Mining` and then add a setting by clicking `+` (plus sign) floating action button
    - This assumes you already know how to setup a miner but if you're not yet familiar, you can check the [links below](#other-references)
5. From the bottom part, you'll see the `MONITORING` switch, enable it
6. Choose the `MONITORING SERVER` you just created from the `dropdown listbox`.
    - the IP ADDRESS and PORT number should appear correctly and then save
7. From the main screen, go to `Mining` then click `START` to run the miner.
    - the mining status will now be sent to the VerusBox's monitoring server
8. You can now start monitoring your app remotely. Enjoy!


### Sample Setup
<img src="https://github.com/pangz-lab/verus_box-release/blob/master/help_assets/img/setup_monitoring.gif" alt="Monitoring Server Sample" height="800" width="400"/>

## Setup VerusMiner to start mining on boot
### 📝Note
- If you have an existing `Macrodroid` setup, please backup your scripts
- The script requires 2 mobile setting to work properly
- Some device setting might have a different setting name as described here but you should find an equivalent one based on your brand and model

### Requirements
#### 📲 Download the following
1. [Macrodroid App](https://play.google.com/store/search?q=macrodroid&c=apps&gl=US)
2. Macrodroid Script → [verusminer_start_on_boot.v2.mdr](https://drive.google.com/file/d/1KpvYCo547cdNrEPYlD9fJAnmwKeYpetV/view?usp=drivesdk)

### 🥓 Part 1 of 2 [ Device Setting Update ]
##### Checkout the following links to get the idea how to setup per brand
1. Hide the device's `bottom navigation bar`.
 - [Samsung One UI](https://www.guidingtech.com/hide-navigation-bar-samsung-one-ui/)
 - [Huawei](https://www.quora.com/How-do-I-hide-the-Navigation-Bar-on-the-Huawei-P30-Pro)
 - [Oppo](https://www.techbone.net/oppo/user-manual/disable-navigation-bar-in-apps)
 - [Mixed Brands](https://deletingsolutions.com/how-to-hide-navigation-bar-android-pie/)
2. Disable the `lock screen`. Your goal here is to remove the lock screen so that when you `turn on` your screen(pressing the power button), you should see the Home screen right away.
 - [Mixed Brands](https://www.asurion.com/connect/tech-tips/how-to-set-up-change-remove-screen-lock-android/#:~:text=How%20to%20remove%20Screen%20Lock,screen%20code%20%3E%20None%20%3E%20Delete.)

### 🧀 Part 2 of 2 [ Macrodroid Installation ]
1. Install `Macrodroid`
2. Open `Macrodroid` and go to `Home` > `Export/Import` > `Import`
 - Note that this import will overwrite all the existing scripts you have so make sure to back it all up to save your existing work.
3. Go to the path where you downloaded the `Macrodroid Script` and then select.
4. A couple of prompts will appear requesting for permissions. Just enable it then continue.(most important part)
5. Go to `Macros`. From there you should see the `Restart Miner on Boot` item
6. Restart your phone to test if it works.
 - During restart, there is a bit of a delay but once the macrodroid icon is active, the script should run within 20 seconds as expected
7. Should you encounter any problem, drop a message in the discord group.

### Sample Script Setup
<img src="https://github.com/pangz-lab/verus_box-release/blob/master/help_assets/macrodroid/script_setup.gif" alt="Macrodroid Script Setup" height="800" width="400"/>

## Questions
### ⛏ MINING
<details>
<summary>❔ Why does the miner connection indicator showing it's disconnected but in the monitoring it's still active?</summary>
<p>

#### 💬 Answer
```
Sometimes when the miner got disconnected from the network, it usually fails to send the appropriate closing message to the server. As a result, the connection is left open leaving the monitoring server thinks that the client is still active refelecting it in the connection indicator.
```
</p>
</details>

<details>
<summary>❔ How long does it takes for the client to connect to the monitoring server when it got disconnected?</summary>
<p>

#### 💬 Answer
```
The main priority of the miner is always the mining. Connection to the monitoring server comes next. When a miner got disconnected, the mining operation would still continue to run. The only time it will care about reconnecting is when the mining status data is collected and ready for publishing. Reconnecting the the server might or might not succeed during the reconnection period but it will retry on the next window time.

So to answer you question, there is no specific timing but the miner will reconnect given the right conditions.
```
</p>
</details>


<details>
<summary>❔ Why is it when I trigger the "Pause Mining" action for some period, some miners did not reconnect instantly?</summary>
<p>

#### 💬 Answer
```
It's due to the device's battery and power optimization setting. Sometimes the countdown timer in the mining device would not work due to this thus failing to restart the miners on time. Try to test it and adjust the settings as necessary.

It's recommended to setup you device with setting optimized for mining. This means removing unncessary apps and services to concentrate all the resources for mining operations only.
```
</p>
</details>

### 📺 MONITORING

<details>
<summary>❔ What are conditions to consider the client as idle</summary>
<p>

#### 💬 Answer
```
It's only when the monitoring service detected the client failing to send mining status data for more than 3 minutes.
```
</p>
</details>

<details>
<summary>❔ Can I turn ON and OFF the monitoring server anytime?</summary>
<p>

#### 💬 Answer
```
YES. The monitoring server is designed to be used this way.
```
</p>
</details>


<details>
<summary>❔ Can I still run the monitoring even if the IP ADDRESS I use is not a static IP?</summary>
<p>

#### 💬 Answer
```
Yes you can but it's recommended to use a static IP ADDRESS. When connected to your network(Wifi), the default IP setting is dynamic. This means,
you can get a new IP ADDRESS different from the one your device used to have at any moment without you knowing it.

For whatever reasons you don't want to set your IP ADDRESS as static, you'll need to update all the client's(VerusMiner) settings to use the new IP ADDRESS you got. That's tedious and beats the purposes of automation.

This setup may vary for each phone brands and models but this will give you an idea how to achieve it.
https://support.honeywellaidc.com/s/article/Android-How-to-set-up-a-static-IP-address
```
</p>
</details>

<details>
<summary>❔ Why can't I see the device in the device selection list?</summary>
<p>

#### 💬 Answer
```
Only active devices are visible from the selection.

If for some reasons the available device becomes idle or inactive while in the middle of performing an operation(update setting, pause mining etc.,), it will still proceed but will likely fail.
```
</p>
</details>

<details>
<summary>❔ Can I run mulitple monitoring operations one after another without waiting for the previous operations to complete?</summary>
<p>

#### 💬 Answer
```
Yes you can. However, keep in mind that each client is designed to receive and execute a single command at a time. Running multiple operations in a single client without considering the ongoing operation is allowed but is very likely to fail as it will not be handled anymore by the receiving clients.
```
</p>
</details>


## Other References
1. [VerusBox Mining](https://youtu.be/7M8Bwz52d7A)
2. [VerusBox Setup](https://youtu.be/Uq97hCHUYwA)
3. [Mining Pool Server](https://youtu.be/CF5O-revXIE)
