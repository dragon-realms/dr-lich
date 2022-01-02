# Instructions for combining Lich with Genie & Frostbite FE

## General Instructions
Basic steps are as follows:

You need a working lich install https://lichproject.org/download.html#win_storm_wiz_lich (WARNING: do NOT download and use the `lich-4.6.52.zip` file at this link. DR Lich uses a different file.)

Set up dependency in SF https://github.com/rpherbig/dr-scripts/wiki/First-Time-Setup steps 1-3

While connected through SF, run ;e use_lich_fork

that should take 5-10 seconds to swap the version of Lich you're on. Run ;e use_lich_main at any time to toggle back. Then you're basically done with SF. close out if it.

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
  
Then connect to a character via Frostbite like normally.

### Mac OS X / *nix

Open up command prompt
Navigate to your lich directory:
 - ex. 'cd ~/Downloads/lich'

Run Lich.rbw with the following options

  - 'sudo ./lich.rbw --dragonrealms --frostbite'
  
Then connect to a character via Frostbite like normally.

#### Note for RVM users
If you are using rvm, you will want to use rvmsudo to do the sudo call (else you will use whatever ruby version sudo defaults to which will lead to Problems). Setting up rvmsudo is detailed here: https://rvm.io/integration/sudo
 The steps are as follows:
 1. Add `export rvmsudo_secure_path=0` to ~/.bashrc
 2. Add `Defaults env_keep +="rvm_bin_path GEM_HOME IRBRC MY_RUBY_HOME rvm_path rvm_prefix rvm_version GEM_PATH rvmsudo_secure_path RUBY_VERSION rvm_ruby_string rvm_delete_flag"` to /etc/sudoers (careful...)
 3. Comment out `Defaults secure_path=...` in /etc/sudoers
 
Now run `rvmsudo ./lich.rbw --dragonrealms --frostbite`
