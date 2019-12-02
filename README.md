# sono_01
Monitor the state of Sono-Motors Crowdfunding cashflow over time and visualize it.

Sono-Motors announced a crowdfounding campain on sunday night of December 1st in 2019. 
They parted with their investors and turn to backers to ask for 50 Million € within 
the next 30 days. 

This tool will visualize the cashflow over this timepreiode and visualize the groth
of cash. Additionally it is planed to visualize an approximation if the funding goal
can be achived in time.

# Features
* crawler called curlsono which uses curl to read the value shown Sono-Motors with the help of grep, sed and awk
* script which initiates the crawler function and dumps date, time and cash value into the sqlite3 database
* dump_sono.db sqlite3 database for date, time and funding amount 

# Quick start
Download the files into a folder e.g. sono:

``` git clone https://github.com/bytedicer/sono_01.git
cd sono_01
```
Since the script is not automated yet, use screen to run to run it as background process:
``` screen -S sono
watch -n 10 sono-get
```
# General
This is tested on a Ubuntu 19.10 System

