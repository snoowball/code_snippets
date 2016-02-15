## How to enable autocomplete in Windows commandline prompt.  
1. Open RegEdit `Win+R -> regedit -> OK`.  
1. Navigate to registry key `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Command Processor`.  
1. For autocomplete directory names using TAB, change `CompletionChar` to `9`.  
1. For autocomplete file names using TAB, change `PathCompletionChar` to `9`.  
1. If needed, see [this article](http://www.online-tech-tips.com/computer-tips/how-to-turn-on-auto-complete-in-the-command-prompt/) for more detail.
