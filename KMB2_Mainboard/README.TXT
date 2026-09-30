KMB2 Readme:

https://github.com/NeilsVintageComputers/Flex09Computer/blob/main/KMB2_Mainboard/KMB2pic.jpg

The KMB2 motherboard is a modified SWTPC hardware based design made to fit a ATX type PC Case (see note** below).
Designed to be used with the KMP6809 processor board and the KMR64K ram board which do not support greater than 64K address space, I have no flex programs that i wish to use that require over 56K of ram so didn't bother with the extra complexity required,
(not tested yet, but you should be able to use original SWTPC CPU and RAM boards if more ram is required.)

There is also the option of plugging in a ATX power supply, there is circuitry that controls the on/off switching of the power supply. This makes the power supply much cheaper, and easier to,  especially if you will be using a ATX case.
This option does require removing and bypassing the voltage regulators on all cards and MB so only use this option if you do not want to use or test original boards in it as they all have on-board regulators.

Address decoding of the SS30 slots and Baud rate generation are carried out on the MB so the SWTPC MP-ID board is not required.

.
.
**I have discovered that all ATX cases are not created equal!  I designed the MB to fit the open frame type case pictured which had 8 slots, thus the card slot brackets line up with the 8 slots in ths "case".
However I built a extra board up with regulators on for test/repair of original SWTPC boards and discovered that even though the ATX case I used had 8 slots they were offset one slot to the right (or in other words the MB mounted one slot to the left) such that slot 0 (the console serial port card) had no slot opening in the case.
To remedy the problem I redrilled the mounting holes in the bottom of the case, if it had been slot 7 not being accessible it wouldn't have been a problem.
So be aware of this!!

I decided that I would never be able to guarantee the slot placement on every ATX case so don't intend on making changes to the MB at this stage. If for any other reason I do make another version of the MB I will allow for multiple mounting holes.


