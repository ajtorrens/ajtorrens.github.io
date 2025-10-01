---
layout: default # Or a specific 'post' layout if you create one
title: "Custom Maps on Garmin Devices"
date: 2025-10-01 22:00:00 +0100 # Optional: time and timezone
categories: tips, sports, tech # Optional: categorise your post
---

# Steps to get custom maps on Garmin wearables

Need more maps on your Garmin wearable that aren’t already installed? Look no further! This guide will help you locate, download and transfer new maps that work in the exact same way as the preinstalled ones. All on-device courses and navigation should work the exact same. This how-to was heavily inspired by [DC Rainmaker’s great guide](https://www.dcrainmaker.com/2019/08/installing-garmin-forerunner.html) on this, but a lot can change in that time, and a lot of new Garmin watches have been announced! So I took the liberty of updating the instructions. (I did email Ray to see if he wanted to reproduce this on his site to get to a wider audience, but no word back yet!)

**Tested with:** Garmin Fenix 6 Pro Solar, Garmin Fenix 7 Pro Solar

**My setup:** Macbook Pro M1 running MacOS Sequoia 15.3.2, Chrome Browser. I am located in the UK so my device came with European maps preinstalled.

_This was first written in early 2025. I then updated the guidance in August 2025, to take into account changes for my newer Fenix watche. Keep reading below!_

## Steps here

1. Navigate to [https://garmin.bbbike.org/](https://garmin.bbbike.org/)
2. Choose your desired area by choosing on the map or searching.
3. Choose the format to be Garmin Openfietsmap Lite (Latin 1), and add your email address to receive the extract. Click Extract.

	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig1.png" | relative_url }}"
       alt="Choosing the target area in bbbike.org."
       class="img-medium">
  		<figcaption>Choosing the target area in bbbike.org.</figcaption>
	</figure>

	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig2.png" | relative_url }}"
       alt="Confirmation that your extract is being processed (and option to donate!"
       class="img-medium">
  		<figcaption>Confirmation that your extract is being processed (and option to donate!)</figcaption>
	</figure>

4. You should receive an email like the following:

	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig3.png" | relative_url }}"
       alt="Email with link to extract in .zip format."
       class="img-medium">
  		<figcaption>Email with link to extract in .zip format.</figcaption>
	</figure>


5. Download the zip from the email. Extract the zip, and isolate the `gmapsupp-*.img` file. This is the disk image of the maps. Rename it so you can distinguish it from any others. I'd recommend the region you've chosen :)

	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig4.png" | relative_url }}"
       alt="Double-clicking on the .zip file gives the folder with the same name, where the maps are located."
       class="img-medium">
  		<figcaption>Double-clicking on the .zip file gives the folder with the same name, where the maps are located.</figcaption>
	</figure>

	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig5.png" | relative_url }}"
       alt="Contents of the uncompressed directory, including the all-important .img file."
       class="img-medium">
  		<figcaption>Contents of the uncompressed directory, including the all-important .img file.</figcaption>
	</figure>

6. (For Mac) Download [OpenMTP](https://github.com/ganeshrvel/openmtp) from github. This will be how you add the file to your garmin system.
7. Open OpenMTP, and connect your watch to your computer with the cable.
8. Open the downloaded `.img` file on one side, and Root > GARMIN on the other side. _[Edit August 2025 when testing with Garmin Fenix 7 Pro]:_ There are many reasons why OpenMTP may not recognise your device. [Read about the issues linked on the github page.](https://github.com/ganeshrvel/openmtp/issues/276) What worked for me was ensuring that Garmin Express--which can be used to transfer **official** Garmin maps and updates--was completely closed, and not running in the background (Activity Monitor) on my Mac. Then, when restarting OpenMTP, my watch was recognised.

	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig6.png" | relative_url }}"
       alt="UI of OpenMTP. You can see the pre-existing map images on the RHS, already stored on the device."
       class="img-medium">
  		<figcaption>UI of OpenMTP. You can see the pre-existing map images on the RHS, already stored on the device.</figcaption>
	</figure>

9. You should be able to easily move the `.img` across, by dragging and dropping. Depending on the size of the file, it may take some time.
	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig7.png" | relative_url }}"
       alt="Transfer process of .img map file from computer to device"
       class="img-medium">
  		<figcaption>Transfer process of .img map file from computer to device</figcaption>
	</figure>

10. When you disconnect the watch, it will say ‘Loading Maps…’
	<figure>
  		<img src="{{ "/assets/images/garmin-tips/fig8.jpg" | relative_url }}"
       alt="Behaviour of watch immediately disconnecting from the computer"
       class="img-medium">
  		<figcaption>Behaviour of watch immediately disconnecting from the computer</figcaption>
	</figure>

11. Done! The map should just load and function as expected when you navigate within the area you defined.

This is a trail in Yosemite National Park, California, as an example.
<figure>
		<img src="{{ "/assets/images/garmin-tips/fig9.jpg" | relative_url }}"
   alt="Examples of how a GPX Route (created in Strava) appears using the new map"
   class="img-medium">
		<figcaption>Examples of how a GPX Route (created in Strava) appears using the new map</figcaption>
</figure>
<figure>
		<img src="{{ "/assets/images/garmin-tips/fig10.jpg" | relative_url }}"
   alt="Examples of how a GPX Route (created in Strava) appears using the new map"
   class="img-medium">
</figure>
<figure>
		<img src="{{ "/assets/images/garmin-tips/fig11.jpg" | relative_url }}"
   alt="Examples of how a GPX Route (created in Strava) appears using the new map"
   class="img-medium">
</figure>


## Update August 2025

I lost my Fenix 6 Pro (I will tell the story elsewhere), and so when I received my Fenix 7 Pro I went through the same procedure to download some extra maps. What I discovered is that many more maps are available for free from Garmin for the 7 Pro series compared to the 6.
For the 6, typically the region you bought the device in was free (e.g. Europe for Europe, US for US etc.) and you had to pay for others (or download open source versions as above). However, for the 7, you get the option to download more for free. You can use [Garmin Express](https://www.garmin.com/en-XD/software/express/) to do this. You can see the list of regions I can add below. Note that some cover less than a single country, some cover just one country, and some cover whole subcontinental or continental regions! 
Most are self-explanatory except for:
- China ML - China Mainland
- SGMYVNPH - Singapore, Malaysia, Vietnam, Philippines
- THID - Thailand and Indonesia

You can download these via the watch (when charging and connecting to WiFi) but it’s quicker to do via the computer and [Garmin Express](https://www.garmin.com/en-XD/software/express/). This is probably also the quickest way to get updates, including the pre-installed ski and golf maps.
There are some notable exceptions, like India. I actually have a trip to India upcoming so I started to look for a non-Garmin version. This led me to the [https://garmin.opentopomap.org/](https://garmin.opentopomap.org/) website. This, in effect, can replace steps 1-4 above. You choose your region, and download the ZIP straight away. It tells you the download size, and gives you the option to add contour lines (I haven’t tested this yet). You can then extract the `.img` from the zip and add to the watch via OpenMTP as before. Word of Caution: The watch can only connect to one programme at a time. For OpenMTP to correctly find and display the watch, you need to fully quit Garmin Express and stop any background activities. OpenMTP is a free open source app, implying there’s no obligation for the author(s) to fix any issues, but [best-effort advice for troubleshooting is described on GitHub](https://github.com/ganeshrvel/openmtp/issues/276).

Once I’d downloaded the India region above, and copied it to the device, you can verify that it had transferred correctly by checking in the watch's maps settings (Settings > Map > Map Manager). Your new map should be in the list.

<figure>
		<img src="{{ "/assets/images/garmin-tips/fig12.jpg" | relative_url }}"
   alt="New map info on the watch"
   class="img-medium">
		<figcaption>New map info on the watch</figcaption>
</figure>
<figure>
		<img src="{{ "/assets/images/garmin-tips/fig13.jpg" | relative_url }}"
   alt="Example of the new map when viewing a premade course."
   class="img-medium">
		<figcaption>Example of the new map when viewing a premade course.</figcaption>
</figure>
<figure>
		<img src="{{ "/assets/images/garmin-tips/fig14.png" | relative_url }}"
   alt="Mapping options available from Garmin Express 1/2"
   class="img-medium">
		<figcaption>Mapping options available from Garmin Express 1/2</figcaption>
</figure>
<figure>
		<img src="{{ "/assets/images/garmin-tips/fig15.png" | relative_url }}"
   alt="Mapping options available from Garmin Express 2/2"
   class="img-medium">
		<figcaption>Mapping options available from Garmin Express 2/2</figcaption>
</figure>



