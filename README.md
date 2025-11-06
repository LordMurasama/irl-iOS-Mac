# IRL-iOS-Mac (forked from: https://github.com/Naginreed/irl-cae_iOS-Mac)
> Belabox Cloud Setup for iOS (Moblin) and Mac OBS (For Translation)
> Japanese Translation Branch: (https://github.com/LordMurasama/IRL-iOS-Mac/tree/LordMurasama-patch-1)

# General Info
This Guide describes a **Low Cost and Easy** Solution for
- better user viewing experience for **IRL**-Streaming 
- **iOS** as Streaming Phone
- **macOS** as Home PC (Mac Intel or Apple Silicon)

> [!NOTE]  
> There are completely "free" methods, but they require more technical expertise and if wrongly configured, could be a security risk for your Mac.
> With this method, you don't purposely open any holes in your network and system security. *(No fixed IP | No Port Forwarding | No Firewall Changes)*.
> Additional security/privacy details here: (https://techdump.murasama.net/2024/06/30/naginreeds-moblin-to-twitch-guide/#security-and-privacy)

---
## Map

<img src="https://github.com/Naginreed/irl-cae_iOS-Mac/assets/71943093/c420ab6e-570c-47de-950a-c08653ec5847">

---

# 1 - Streaming Phone  

> [!NOTE]   
> If you have multiple phones, please use the newest/best performing one as the Streaming Phone

1.a - Follow this [Youtube Guide](https://www.youtube.com/watch?v=GbR0xfpJXJE) to install Moblin and set it up for direct Twitch Streaming _(as Backup)_

---
# 2 - SRT/SRTLA Relay

> [!NOTE]   
> This Server takes the Two SRTLA Streams and combines them into one SRT Stream as seen on [Map](#map)

> [!IMPORTANT]   
> This Service costs $10 USD.

2.a - Create an Account with [Github](https://github.com/signup) *(If you already have one skip to Login)*
 - You then need to Verify your E-Mail Address and [Login](https://github.com/login)

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/bafd6a15-7ec2-4f3e-8a1f-7737e41d9a8f" height="600">

2.b - Once logged in open the [Belabox Sponsorship](https://github.com/sponsors/rationalsa) Page  
 - Scroll down and select the **$10 a month** Tier which includes 1x SRT/SRTLA Relay Server
 - Fill out your Billing Info and setup your Payment Info *(Only Credit Card or Paypal supported)*
 - Alternatively you can also let your Viewers buy [Vouchers](https://shop.belabox.net/product/belabox-cloud-voucher) for multiple Months.

2.c - Once you either sponsored or have a voucher, open the [Belabox Cloud](https://cloud.belabox.net) Page and
 - Login/Authorize with your Github Account  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/5385a7b6-e1c4-42ac-a5a1-729cf53dc732" height="600">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/f8b19ac5-7862-4097-8701-78001048d003" height="600">

2.d - On the Top of the Page press the **3 Lines** then **SRT(LA) relays**

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/4c33128e-253c-493e-8d40-2c19e67a2389" height="600">

2.e - Click on **Add** and change the Name. Change the **Server** to your **closest Location**

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/8425c1a1-add3-40d1-8082-b03312429539" height="600">

2.f - Scroll down until you see **Moblin Settings** and tap the **Add automatically to Moblin** Button to automatically add the right Info in Moblin.  

---
# 3 - Streaming Phone
3.a - Open the **Moblin App** and go to **Gear** Symbol *(Settings)* on the top right  

<img src="https://github.com/Naginreed/irl-cae-setup-ioS/assets/71943093/f0723f0a-53a1-441d-990c-00a88d0349f3" width="600">

3.b - Go to **Streams** and then tap the **Belabox Cloud** one  
3.c - Go to **Video** and set the following settings  
 - **Resolution:** 1920x1080p  
 - **FPS:** fixed 30fps  
 - **Bitrate:** 4500 kbps  
 - **Codec:** HEVC(h2.65)

3.d - Go back and **toggle on Twitch** and tap on it to enter. Set your Twitch Name and Twitch ID. *(You can get the ID from [here](https://www.streamweasels.com/tools/convert-twitch-username-to-user-id/))*  
3.e - Next you'll want to add your Alerts to Moblin. You will need to go into your Alerts Dashboard via a Web Browser  
 - [Streamlabs](https://streamlabs.com/dashboard#/alertbox) and copy the Widget URL

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/255e3ef7-cbd5-4cfa-84a8-17d68c78ccb6" height="600">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/82365cc6-ade2-458f-b583-ccad4b0b62f1" height="600">

3.f - Switch back to Moblin and go to the **Settings** Screen. 
 - Tap on **Scenes** then on **Widgets** then **Create**. 
 - Name it **Alerts**  

3.g - Set type to **Browser**  
 - paste the Widget URL into **URL** Field.  
 - Set Width to 600 and Height to 400 *(change the size if the Alerts are wrong size)*  

3.h - Go back to the **Scenes** Menu and tap on **My scene**   
 - Then tap **Add Widget** and choose the **Alert**-Widget we just created.
 - Make sure its on the Top of the List.  

3.i - Go back to the **Main View** and **check** that **Chat** is loading and Test that **Alerts** are **working**  
 - Streamlabs *(Test-Alerts are available in the Dashboard)*  

---
# 4 - Mac-PC
Any normal Mac or MacBook can be used (with hardware encoder/decoder for better stream performance), best cabled directly to your Home Internet Router.
> [!WARNING]  
> This Mac needs to have a **STABLE** Internet Connection during the whole stream with at least 6Mbit Upload *[Speedtest](https://www.nperf.com)*

## 4.1 OBS
> [!NOTE]  
> This is the Program that gets the Stream from the Relay Server and converts it back to old RTMP/h.264 Standards and streams it directly to Twitch. Here you have a lot of Options to set Videos, Text, Music to engage/entertain your viewers while you reconnect

4.1.a - **Download [OBS Studio](https://obsproject.com/download)** for your System  
4.1.b - **Install OBS** Studio and **Launch** it.

> [!NOTE]: Update the info to the Mac specific ones from: (https://techdump.murasama.net/2024/05/22/obs-studio-mac-installation-section/)

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/3555ea78-d6bd-440b-9bdc-15a91799f1a2" width="400">

4.1.c - In the Auto-Wizard 
 - Optimize for Streaming
 - **Resolution:** 1920x1080
 - **FPS:** 30
 - **Service:** Twitch
 - Connect Account
 - Log in the newly popped up Window.
 - Uncheck the **Estimate bitrate** and enter manually **5900** *(7900 if you're Twitch Partner)*
 - **Finish** the Wizard

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/a6164a26-5ba9-4219-9c22-c2eb6abfa0e1" height="400">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/bafb9a3c-1d6e-4909-9c78-d0381c521b30" height="400">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/4bf17fc2-00ad-40b0-b262-0334f62d978a" height="400">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/c7e714a3-fd5a-4783-aaff-9c82ea227f59" height="400">

4.1.d - **In OBS** on the bottom left **add** now following **scenes**
 - Start
 - Live
 - Low
 - Brb
 - End

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/344aaedc-92df-41c1-9e65-1dd6223deb0d" width="600">

4.1.e - Click on the Live Scene, and add a **Media Source** and with name **Belabox Cloud**. 
 - A new Window with settings will open

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/dedc65b3-03c6-4ad0-a2f6-ef907ff541cc" width="600">

4.1.f - Open the **[Belabox Cloud](https://cloud.belabox.net/#relays)** Page  
 - go to **SRT(LA) relays** and
 - scroll down until you see **OBS Media Source Settings**

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/d6669e01-035c-4879-aa2e-df7ebe333b9a" width="600">

4.1.g - **Go back** to **OBS** and **set** the **same settings**
 - Uncheck Local File
 - Set Network Buffering to 1 MB
 - Copy Input from Belabox Cloud Page
 - Set Reconnect Delay to 2S
 - Check Close file when inactive

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/fb5d68c6-b45b-4b40-8f70-ad1aaf224e78" width="600">

4.1.h - Right-click on the **Belabox Cloud**-Source, then **Transform** and **Fit to Screen** *(or select it and hit CTRL+F)*  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/c993bb43-a3ea-4bc5-a75a-c46858d2305e" width="600">

4.1.i - Then Copy *(Command+C)* the **Bellabox-Cloud**-Source over to the **Low** Scene  
4.1.j - Go To **Settings** on the bottom right. In the new Video select **Audio** and **Disable all Global Audio Devices**  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/20b58802-fc64-491d-9d74-3bd0aef2d93d" width="500">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/87a30f26-a525-47c2-9427-b0a1ffbe7067" width="500">

4.1.k - On the top menu bar click on **Tools** then on **Websocket Server Settings**. Check the **Enable WebSocket Server** and hit **OK**  

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/cec9078c-a2e2-45dc-9bec-24041f19a98f" width="500">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/918e7d93-3191-4080-b5e3-3d1c8c4b9d85" width="500">

---
## 4.2 NOALBS
> [!NOTE]  
> This is the Program that samples your connections bitrate (via a stats process) and controls OBS via Chat-Commands and automatically switches Scenes if Stream from the Phone hits a configured low bitrate or lost connection.  The program is unsigned and and will display a Windows UAC dialog box about this.  Please run this program at your own risk (it is open source, used by many, and there have been no reports of any malware associated with it).
>
> Update this information with the Mac NOALBS info from here (important security related information): (https://techdump.murasama.net/2024/05/23/mac-noalbs-installation/)

4.2.a - **Download [NOALBS](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching/releases)** for your System and unpack them to a location of your liking *(i recommend making a Stream and then a NOALBS Sub-Folder)*  
4.2.b - Inside this Folder you should have these 4 files  
 - .env
 - config.json
 - noalbs
 - launch.sh

Sometimes .env will not show or download due to the . in the name
[.env](env)
Just Download it from here again and place it in the same folder

4.2.c - Open up a Terminal Window and enter command
`cd /Users/`yourusername`/Documents/Stream/NOALBS`
where **yourusername** = your username on the Mac and the Path to the folder, if you have a different one. Then hit **Enter**
`mv env .env` and hit **Enter**
env File should now vanish in Finder *(You can show it in Finder by pressing* **Command + Shift + .** *)*

4.2.c - For NOALBS to respond to our Chat commands, we need to give access to a Twitch Account (it is suggested to create an alt Twitch account and use that for the following; you can enable the creation of additional accounts from your Twitch Settings under Security and Privacy and toggling on "Enable additional account creation".  Make sure to /mod this account. Once you are logged in with your preferred Account in Twitch, click on this **[Link](https://b3ck.com/twitch/oauth)**, then hit **Authorize with Twitch** and copy the whole Code from the website

<img src="https://github.com/user-attachments/assets/d668b651-5f7e-45b3-9e1a-e26eb5174b19" height="300">
<img src="https://github.com/user-attachments/assets/44ca3f4b-4ea8-47a8-868e-180fc5c62ba7" height="130">

4.2.d - **Open** the **.env** File with a Text-Editor
 - replace everything with your copied data

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/33dabd80-1a70-4ac1-8451-b942200767b0" height="40">

 - save and close the file

4.2.e - Download the File and replace it with your **config.json**  
[config.json](config.json)  
4.2.f - **Open** the **config.json** File with a Text-Editor  
 - replace all 3x of *REPLACE_STREAMER_NAME* with your Twitch Account Name

4.2.g - open the Open the **[Belabox Cloud](https://cloud.belabox.net/#relays)** Page and go to **SRT(LA) relays**  
 - Scroll down to **NOALBSv2 configuration**
 - replace *REPLACE_BELLABOX_URL* with the URL from the Belabox Page
 - replace *REPLACE_BELLABOX_INGEST_KEY* with the last Part of the URL
 - NOTE: make sure to keep your Websocket connection information safe (never share or reveal that info off/on stream)

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/fe194e73-c223-4327-9680-af1b570869b1" height="350">

4.2.h - Go back to OBS into the Websocket Settings and click on **Show Connect Info**. 
 - Copy the **Server Password**
 - replace *REPLACE_OBS_WEBSOCKET_PASSWORD* with the copied data

<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/ab6652a4-7ff0-41f6-8746-1290e2d243ba" height="200">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/7f04f75c-0611-43d6-8831-5fc8487981db" height="300">
<img src="https://github.com/Naginreed/irl-cae-setup/assets/71943093/f16885ce-8c51-4bb4-92fa-b0e7311f3b41" height="100">

4.2.i - Save and close the file. *Detailed Infos [NOALBS Github](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching)*  
4.2.j - Start the **noalbs** programm. *There should be an error starting it the first time saying that the developer is not verified, just hit ok*  
4.2.k - Make sure .sh files are **always opened** with the Terminal app. To do this Control Click the .sh File > Open with > Other. In the Menu by **Enable** choose **All Applications** and check **Always open With** below. Then choose **Terminal** on the left side and hit **Open**

4.2.l - Always run NOALBS via the launch.sh file. Check if it shows any Errors. Errors with Chat -> check the .env file.  Errors with OBS -> check OBS Websocket or Websocket Settings in config.json  

> [!NOTE]  
> Opening the launch.sh in the Terminal app will always start up NOALBS from within the directory it is in.

> [!TIP]
> You can also make an Alias to the launch.sh and put it on the desktop to not forget to run it.

---
# 5 - Make OBS pretty
We are finished with the basic Setup, but the Scenes are basic placeholders.
The following is an Explanation on what Scene is used for, and what People normally place in them.  
> [!NOTE]  
> Following are just recommendations. Feel free to design however you want.

**Start**
- Every time the Stream starts with this scene until the phone is live
- Video+Music is often used as Background
- simple Text "Starting Soon ..."

**Live**
- As soon as there is a connection from the Phone to OBS this will be shown
- No additional things needed, since Overlays should run on the Phone

**Low**
- When connection to the Phone is bad quality
- simple Text "low bitrate"
  
**Brb**
- When the connection to Phone is lost completely or you end the livestream in Moblin on purpose *(for privacy)*
- old VODs or Clips are often used (For Clips, the suggested recommendation is a Folder named Clips and adding a VLC Media Source *requires [VLC Media Player](https://www.videolan.org/vlc/)*)
- simple Text "Be right back"
- Can be switched to when you go to the restroom or have private Conversation for a few Minutes
  
**End**
- Can be activated by typing !end in Twitch-Chat
- Similar to Starting Video+Music
- Simple Text "Ending Stream"

---
# 6 - Normal Operation 
> [!NOTE]  
> Before **every** IRL-Stream, you need to do the following

6.a - **Start** your **Mac** at Home an make sure it has a Internet Connection and that it doesn't turn off automatically  
6.b - **Start OBS & NOALBS** on your Mac  
6.c - **Go outside** to where you want to start your IRL-Stream  
6.d - Enter `!start` in **Twitch-Chat** to start Stream to Twitch  
6.e - **Go Live in Moblin** -> after a few seconds you are switched to **Live-Scene**  
6.f - If you stop or lose connection on the Phone -> after a few seconds you are switched to **Brb-Scene**  
6.g - As soon as connection from Phone to Internet is restored -> after a few seconds you are switched back to **Live-Scene**  
6.h - End/Start the Livestream manually in Moblin to switch between `!brb` and `!live`  
6.i - **Stop the Stream** automatically if you raid someone or with Chat command `!stop`  

> [!IMPORTANT]  
> With every Scene Change in OBS you will see a text Message in Chat

---
# 7 - 2nd Internet Connection  
> [!NOTE]  
> This is optional and improves stream stability alot in many cases. But it doesnt prevent outtages in No Service Areas like deep into the Mountains or Tunnels.

As seen in the [Map](#map) there can be 2nd Internet Connection for your phone to reduce the chance of outtages for the Live Stream.  
Either a Mobile WiFi Router or a Second Phone with Mobile Hotspot active.  

> [!IMPORTANT]  
> For this second SIM a different Provider is highly recommended.
> The 2nd Sim will also consume about ~50% of the overall Data

---
# 8 - Stream directly to Twitch  

If for whatever reason the Relay or Home Mac is not working, you can easily switch back to direct Streaming in the Moblin App.  

8.a - Got to **Settings** > **Streams** and Create  
8.b - Tap on Twitch an follow the instructions  
8.c - Go to **Video** and set the following settings  
 - **Resolution:** 1920x1080p  
 - **FPS:** fixed 30fps  
 - **Bitrate:** 5800 kbps  
 - **Codec:** h.264

8.d - Go back then **toggle on Twitch** and tap on it to enter. Set your Twitch Name and Twitch ID. *(You can get the ID from [here](https://www.streamweasels.com/tools/convert-twitch-username-to-user-id/))*  
8.e - Go back to **Settings** > **Streams**. Deactivate Belabox and activate Twitch

---
# 9 - Additional Help  
### Moblin App 
Here is their [Discord](https://discord.gg/Tm6kf778)
### OBS 
you can check their [Forum](https://obsproject.com/forum/) or just look up one of the hundreds of Youtube Tutorials
### NOALBS
Here is the Guide on [Github](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching) and their [Discord](https://discord.gg/efWu5HWM2u)

