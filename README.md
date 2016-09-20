# Instructions for combining Lich with Genie & Frostbite FE

## General Instructions
basic steps are as follows, you need a working lich install https://lichproject.org/download.html#win_storm_wiz_lich 

Set up dependency in SF https://github.com/rpherbig/dr-scripts/wiki/First-Time-Setup steps 1-3

While connected through SF, run ;e toggle_lich_fork

that should take 5-10 seconds to swap the version of Lich you're on. Run that command again at any time to toggle back. Then you're basically done with SF. close out if it.

## Genie-specific instructions
Get your genie client open

Open up an administrator command prompt (win+x then A in windows 8+)
navigate to your lich directory and in the command prompt run 

 - 'ruby lich.rbw --dragonrealms --genie'
  
Then connect to a character via genie like normally.

You should have lich access, the only difference will be it uses , instead of ; as it's special character since Genie does parsing on ;

If you disconnect from that character (even keeping genie open) you'll need to run the command again in the command prompt.

## Frostbite-specific Instructions

Download Frostbite from: http://matoom.github.io/frostbite/installation.html

### Windows 
Open up an administrator command prompt (win+x then A in windows 8+)
navigate to your lich directory and in the command prompt run 

  - 'ruby lich.rbw --dragonrealms --frostbite'
  
Then connect to a character via genie like normally.

### Mac OS X / *nix

Open up command prompt
Navigate to your lich directory:
 - ex. 'cd ~/Downloads/lich'

Run Lich.rbw with the following options

  - 'sudo ./lich.rbw --dragonrealms --frostbite'
  
Then connect to a character via Frostbite like normally.