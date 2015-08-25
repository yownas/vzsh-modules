# vzsh-modules
Small scripts (modules) that could be used via vzsh.

Usually called with: vzsh -M \<modulename\> \<arguments\>

To use these scripts you need vzsh from https://github.com/yownas/vzsh

## wol - Wake On Lan

    vzsh -M wol <vzhost>
    
Anything beyond the first word in the hosts file used by vzsh is a comment. This module let you store the
MAC-address there and use it to send wake-on-lan packages to power up vzhosts that has been turned off.

Add the addresses like this:

    vzhost1 12:34:56:78:90:ab
    vzhost2 1234567890ac
    vzhost3 DE:AD:BE:EF:13:37

And remember to set the command to use for sending packages in the script, nc or socat and set the broadcast
address to use.
