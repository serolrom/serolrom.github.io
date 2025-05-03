---
title:  "Broke and fixed pacman db.lock"
layout: post
---
My today's pacman update was interrupted by an error like "(unable to lock database)".  
I didn't get too nervous. I trust Timeshift. But before rolling back, and since I have a way to fix it, I'd rather try and troubleshoot. That's what driving Arch is about, right? Let's see how long do I last in this mood.  
I leave it documented here for my future reference.  

I end up being happy to try the troubleshooting path. The troubleshoot for this one, as you probably suppose if you are a usual Arch driver, is no big deal.  
My approach is to rely on the Arch Wiki/forum. I've been sold the idea that the Arch Wiki and community are as much part of the distro as the kernel itself.  
Almost on the first try I find someone dealing with this problem, and the fix is to remove the db.lck file.  
# rm /var/lib/pacman/db.lck  
I did not remove it though, but renamed it, just in case, as at this point I don't know what this file is. It works. Too easy, but I'm not complaining. It's taken so little time that I'd better some supposedly troubleshooting time investigating a bit more, and I regret not having gone to the [Wiki](https://wiki.archlinux.org/title/Pacman) instead of the forums.

db.lck is a file that only exists if and when pacman packages database is being updated, so that no other process will conflict, and it is deleted when finished to let any potential other process take the chance. If the process in control is interrupted, the file may not be deleted, preventing further updates.  

Now, before removing the db.lck file, it would be advisable to make sure that a process is not actually running and guilty of it, as the wiki says: _"Tip: You can run fuser /var/lib/pacman/db.lck as root to verify if there is any process still using it."_

Another thing learned. Now I can resume normal life. I'm getting attached to Arch and I'm thinking of making it look nice.
