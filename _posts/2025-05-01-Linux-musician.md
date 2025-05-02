---
title: "Linux musician"
layout: post
---
Today I plugged the laptop and I started Firefox, but I only got to 'high level' domains. For example, I could get to mozzilla.org, but then when getting deeper, line in Mozilla accounts, the browser did not reach. I could get to YouTube, but not start session. Crap!  
I followed Gemini instructions and started NetworkManager.  
I queried wifis with "# nmcli dev wifi", then tried to connect to my wifi with "nmcli dev wifi connect WIFI_NAME password MY_WIFI_PWD", but it stated my password was not correct.  
However a system message after a few moments told me "disconnected from wifi" and I couldn't even ping anything, a moment later another system message tol me "connected to wifi" and now I can browse anything.  
I proceed to enable NetworkManager to make the configuration persistent.  
I check my /etc/resolv.conf file and it has changes made by NetworkConfig by some dark magic.  
  
Note: before having a GUI, I had to leave NetworkManager disabled! if I enabled it, I could not ping and download things or get git repos. Now NetworkManager has fixed my connection AND I can ping anything.  
I don't understand completely what happened, but I leave it here documented for future reference.  
  
I use Arch, btw.  
	sergio @May 1st, 2025  
  
Later on, today, I install yay AUR helper. My system gets better by the minute.  
Next, I installed and enabled haveget.service - this claims to make sddm show up faster, but to be honest, I don't have proof of it.  
I installed simpleterminal called 'st' (https://st.suckless.org)  
  
Finally I am getting somewhere. Time to look at plugging in my guitar.  
After searching the web with prompts like "Arch music production", "Configure Arch for music production", etc, I get videos from the "usual suspects". Don't get me wrong, all the material is superb, but with some issues. I liked particularly Unfa's content, but that video where he explains how he configures his Manjaro for music production might be updated. Things seem to have changed rapidly in the last years. Jack was replaced by jack2, an this seems now to be replaced by pipewire.  
So I decided to be consistent with the idea of the Arch Wiki being as good as I claim it to be when I installed Arch, and made a quick search. Turns out, there is a section for Professional Audio. The practical only thing to do is to install the pro-audio package group.  
And that's what I do: "sudo pacman -S pro-audio". This package seems to have everything I'm after, without having to worry about package compatibilities. Better yet, while some words are mentioned in the wiki about compiling a low-latency kernel, it also says explicitly that Arch kernel shouldn't even need it. I'll report back. By now I just can tell I know have a complete set of applications as I found when I installed UbuntuStudio a few weeks ago before embarking in this Arch adventure. It's a bit late today, heading to bed.
