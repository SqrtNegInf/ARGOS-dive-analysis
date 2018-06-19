# ARGOS satellite telemetry dive analysis

This project processes the telemetry from Artic-region whales tagged with 
satellite transmitters that record depth and duration of their dives.  
Geo-tracking was also done, but handled separately from this analysis.

## Logistics of telemetry

The transmitters record information about depth and duration of dives, and when
the whale surfaces, attempts to burst-transmit to any ARGOS satellite available.
Because band-width is very limited, and the whale may spend only a short time at
the surface, the data format used is very compact.  When ARGOS comes in range of
a ground station, the data is downloaded. Eventually batches of accumulated data 
from a given tag are made available to end-users.

## Processing telemetry

To produce the Excel-style format required by the end-users, the dive analysis 
software must 'decode' the terse telemetry format, and handle the following conditions:

* data drop-outs
* duplicate data
* garbled data

After this step, the sanitized data is processed to provide derived information
of interest to marine-mammal biologists and wildlife managers, such as 

* descent and ascent dive-rates
* maximum dive depth
* dive duration
* time spent in dive-depth 'bins'
* non-feeding intervals

and so forth...

## Whales and technology

For this project, the whales tagged were belugas and narwhals around Greenland
and in the Canadian high Artic.  The focus of the research was to investigate
the depth and duration of their dives, as this yields information about their
feeding behaviors. The transmitter technology is from from Wildlife Computers.
More information available at the Web site <http://www.wildlifecomputers.com>
