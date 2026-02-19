## usals - Southern Hemisphere Edition!

This is a patched version of 'usals' for enabling DiSeQ dish positioning for users south of the equator. 
Previously, 'usals' would steer the dish in the wrong direction for us folks down in the southern hemisphere. 
All other functionality is identical to l2mrroberto's usals repository. Tested and working on DragonOS FocalX R35.

## Building
```
cd
git clone https://github.com/RobVK8FOES/usals-southern-hemisphere.git
cd ~/usals-southern-hemisphere
make
```

## Usage Example
```
cd ~/usals-southern-hemisphere
./usals -a 2 -A -12.46 -G 130.84 -W 10 -v -U 108.2

./usals   = Name of binary
-a 2      = DVB-S2 adapter selection
-A -12.46 = Negative 12.46 dish lattitude 
-G 130.84 = 130.84 dish longitude
-W 10     = Waiting time for dish to move (seconds)
-v        = Verbose debug messages
-U 108.2  = 108.2E orbital position
```
Run the binary with the -h argument to see help file:
```
cd ~/usals-southern-hemisphere
./usals -h

Usals tool for the Linux DVB S2 API
(based on blindscan-s2)

usage: usals
        -a number : adapter number (default 0)
        -f number : frontend number (default 0)
        -U N.N    : orbital position for USALS
        -G N.N    : site longtude
        -A N.N    : site latitude
        -W number : seconds to wait after usals motor move (default 45)
        -v        : verbose

Example:
           usals -U 1 -v -G 021.100 -A 055.767 -W 15

```

## Installation
```
cd ~/usals-southern-hemisphere
sudo make install
```
