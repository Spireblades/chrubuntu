# chrubuntu
A step-by-step guide on how to install custom firmware and ubuntu to your chromebook.


<h2>So, I was thinking earlier "what's the best way to unenroll a chromebook?" and then it hit me. Why not install a different OS? So that's what this is for. (I'm lying a little bit, but we all have to lie to get around in life.)</h2>

<h1>Part 1: Unenrollment</h1>

<h2>The first part of this is unenrolling your chromebook, to access developer mode.</h2>

<h4>Step 1: Download a prebuilt shim for your board, here: https://github.com/ading2210/sh1mmer/actions/runs/16721214945</h4>

<h4>Step 2: Flash the shim to your USB using CRU or any other tool (BalenaEtcher is one you can use, and you <em><strong>WILL</em></strong> need it for the rest of this.</h4>
        
<h4>Step 3: After the shim is finished, SAFELY remove it from your computer and enter recovery mode on your chromebook by pressing POWER + REFRESH + ESC.</h4>

<h4>Step 4: Once in recovery mode, press CTRL + D and confirm that you want to enter developer mode (doesn't matter if it's blocked, if you can run shims, you're good.)</h4>

<h4>Step 5: After going into developer mode, re-enter recovery mode on your Chromebook. Insert the flashed USB into your chromebook, and let it work its magic.</h4>

<h4>Step 6: Once you're in the SH1MMER screen, click Payloads, then Br0ker.</h4>

<h4>Step 7: Let it do its thing, then press enter to reboot.</h4>


<h1>Part 2: The Amazing, Exciting, Custom Firmware Palooza! (Sponsored by MrChromeBox)</h1>

<h2>The second part of this involves entering developer mode, after unenrollment, to access a terminal to install custom firmware (CFW)</h2>

<h4>Step 1: After rebooting, do NOT press "get started", instead, reboot back to recovery mode and turn ON developer mode.</h4>

<h4>Step 2: Let developer mode's 5 minutes go on, then boot into ChromeOS.</h4>

<h4>Step 3: After you're in developer mode, go into quick setitngs (bottom right of the screen) and connect to your WiFi network.</h4>

<h4>Step 4: Press CTRL-ALT-FORWARD in that order to open the VT2 shell.</h4>

<h4>Step 5: Sign in as user 'chronos' and don't try entering a password, as one should not exist. If one does, use shimboot to access a Linux terminal, then continue the process below.</h4>

<h4>Step 6: Input this long script into the terminal: <em>cd; curl -LOk mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh</em>, then press enter.</h4>

<h4>Step 7: Once you're on the selection screen, hit 1. Don't hit anything else, as the other options require write protection to be disabled, and this is a guide for people who don't want to disable it.</h4>

<h4>Step 8: Let it work, then quit out of it by pressing Q. After the script is gone, exit the terminal by pressing CTRL-ALT-BACK</h4>


<h1>Part 3: Installing Ubuntu</h1>


<h2>The third, and final part of this, is to download your Linux distro, and install it to your disk!</h2>

<h4>Step 1: Insert your USB back into your computer.</h4>

<h4>Step 2: Download whatever Linux distro you want. Mint, Ubuntu, or Debian work best based on what I've heard/seen/tested.</h4>

<h4>Step 3: Flash the ISO to your USB using BalenaEtcher.</h4>

<h4>Step 4: Once the USB has been flashed again, open your chromebook and go to the developer mode screen. Plug your USB in when you get to the developer mode screen.</h4>

<h4>Step 5: On the developer mode screen, do NOT hit CTRL-D, instead, hit CTRL-L. It will then prompt you to enter a number; enter any one.</h4>

<h4>Step 6: On the bootloader's startup screen, press ESC as soon as the option is given to you.</h4>

<h4>Step 7: Once you're in the interrupted bootloader, go to 'Boot Manager' and hit 'Open from File'.</h4>

<h4>Step 8: With the USB plugged in, select the first partition on your flashed USB.</h4>

<h4>Step 9: Navigate through the boot folders, and select the file named "bootx64.efi". Don't select any of the other files, as I have no idea what they do.</h4>

<h4>Step 10: On the next screen, hit "Try or Install Ubuntu".</h4>

<h4>Step 11: Proceed through the Ubuntu installation process, selecting Interactive installion.</h4>

<h4>Step 12: On the 'Disk setup' screen, make sure to click "Erase disk and install Ubuntu". This is a VERY important step if you don't want to carry a USB with you everywhere you go.</h4>

<h4>Step 13: Wait for Ubuntu to finish installing, then unplug the USB. Don't panic! This is normal. Restart the computer using POWER+REFRESH.</h4>

<h4>Step 14: Load the bootloader, but this time, don't press ESC to interrupt it. If everything went well, the bootloader should automatically load Ubuntu!</h4>


<h1>Congratulations!</h1>


<h2>You now have invalidated any shred of integrity you may have had left. But, we're exploiting school chromebooks, so... I guess there wasn't much left anyway :skull:</h2>


<h5>Special thanks to codenerd87 for being especially patient with me during this entire process and helping me figure out the do's and dont's of this. If you need help, I recommend asking them (or anyone else for that matter lmao), and to MrChromeBox for making the RW_LEGACY CFW.</h5>
