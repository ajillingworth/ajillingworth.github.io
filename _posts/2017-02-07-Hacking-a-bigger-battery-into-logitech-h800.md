---
title: How to Hack a Bigger Battery into your Logitech H800 Headphones
---
So you love your Logitech H800 headphones because:

1. Your sound quality is great
2. Your microphone quality is great
3. They fold up really small and are very light for travelling
4. They connect effortlessly to your phone over Bluetooth.
5. They connect to your laptop using a proprietary USB key, and so bypass all of the compromises of Bluetooth devices:
  * No manual switching between headset and headphones mode
  * Better range
  * Better quality sound while on phone calls
 
But, the battery life doesn’t last a full work day, and it beeps really loud when it starts running low.
 
If that all rings true, then you’ve come to the right place.

Disclaimer: before we get started, here's a quick reminder that you shouldn't trust random internet people. I'm probably completely incompetent. You shouldn't follow my advice and strap a bunch of volitile chemicals to your head.
 
## Step 1 – Get lots of stuff
 
- Some heatshrink cable wrap
- A 10kΩ resister
- Soldering iron
- Solder
- A molex picoblade connector
- A Dremel (totally buy a Dremel rather than using a combination of pliers and a drill)
- A bigger battery (https://www.amazon.com/gp/product/B00MZJBQHU/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1)
- A pair of Logitech H800 headphones
- A solid workbench (definitely not your coffee table or the fireplace - DO AS I SAY AND NOT AS I DO!)

![My coffee table covered in crap]({{ site.url }}/assets/BatteryHack/workbench.jpg)
 
## Step 2 – Hack off lots of plastic pieces from inside your headphones
 
Hack off all the bits in red from inside the battery slot using your dremel (definitely not your drill and pliers)

![Hack off enough bits until the battery fits]({{ site.url }}/assets/BatteryHack/bits_to_hack_off.jpg)
 
## Step 3 – Solder all the things!
 
Helpfully the Molex Pico blade connector you have has the colors in a completely different order than the connector within the headphones…
 
So, red means yellow, white means black and black means red... obviously.
 
![Lots of color mismatches]({{ site.url }}/assets/BatteryHack/color_mismatches.jpg)

The middle wire of the original battery (white, now black) should be connected to an internal temperature sensor within the battery. This usually allows the charging circuit in the headset to monitor the battery’s internal temperature in order to prevent it from overheating. The new battery that we just bought doesn’t have a temperature sensor. it still has a safety mechanism that will shut it down in the event of overheating. Don’t worry, as everyone always says, you can always trust an internet stranger with your personal safety.

![New battery]({{ site.url }}/assets/BatteryHack/new_battery.jpg)

However, the headset won’t charge the battery if it can’t read how warm it is in there.
 
So how do we solve this? The temperature sensor is implemented as a variable resistance between the ground wire and the sensor. So let’s measure the resistance between the temp sensor and ground. At room temperature, it’s around 10kΩ, so it’s fairly likely if we just put a 10kΩ resister between ground and the middle wire, that will make the headphones think that the battery is always running at a normal temperature and allow it to charge. 100% certified safe! (probably...)
 
So, let’s start by slipping on the heat shrink wrap. Then let’s solder the black wire to one leg of the resister.

![Terrible solder job]({{ site.url }}/assets/BatteryHack/terrible_solder_job.jpg)
 
At this point, you realize that you’re really crap at soldering stuff and you’ve already shrunk the heat shrink wrap. So pull it all apart and do it again.

![One half done]({{ site.url }}/assets/BatteryHack/one_half_done.jpg)
 
Now that you've resoldered and used your heating element (and totally not just run the soldering iron over a few times, releasing the lovely smell of burning plastic) to shrink the plastic wrap, we need to work on soldering the other end of the resister to our ground (which is a lovely, and totally not confusing, red color).
 
Next step is to connect the ground from the battery (black) to our (red) ground. We use a larger gauge heat shrink wrap to cover over the whole thing.

Now we have a straight forward solder between the positive terminal from the batter (red) and the positive on our Molex connector (yellow). Rinse and repeat with the heat shrink wrap.

![Battery all soldered]({{ site.url }}/assets/BatteryHack/battery_all_soldered.jpg)
 
## Step 4 – cramming and more hacking
 
Finally – cram the whole thing into the battery slot, hacking off any extra pieces of plastic until the battery sits flush and the cover will go on.
 
Simples…

![New battery in place]({{ site.url }}/assets/BatteryHack/new_battery_in_place.jpg)
 
## Step 5 – Test it
 
Test your horrible hack job by sticking the headphones on your head, running them empty, then charging them back up to full.
 
If it doesn’t set your hair on fire a la Note 7 and charges back up again, then congratulations! It’s probably not going to kill you.

Don't worry - it's kitty approved.

![Kitty approved]({{ site.url }}/assets/BatteryHack/kitty_approved.jpg)

OK - well maybe he looks more worried than approving...
