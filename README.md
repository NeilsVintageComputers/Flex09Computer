# Flex09 Computer
An updated re-make of a computer I built in the early 80's.
<img width="1512" height="1969" alt="image" src="https://github.com/user-attachments/assets/7cdb5c51-7d5b-4b4a-af5d-a0cc5c82cc22" />

In the early 80's I built a 6809 based computer based on the SWTPC 6809, the most popular 6809 computer at the time. 
Back then before the internet it took a lot of effort to find the information needed, although schematics were made available by the manufacturer, software was much harder to come by.
I had a disk that a mate, who was also building his own machine, managed to get hold of and modified the Motorola Assist09 monitor to boot the SSSD 5.25" disk.
After quite a lot of learning about configuring Flex to work on my hardware I managed to get it working, it was a great learning experience that really got me interested in playing around with computers.
I only used that computer for about a year before IBM clones became available at a affordable price then it was put into storage and forgotten about.



The computer has since been lost, I am not sure if it is in storage or disposed of, then after finding 3 boxes of disks I had saved I decided to build a reproduction of the computer.
I imaged all the disks with a greaseweazle and only found 3 out of about 30 disks were faulty, not bad for 40 year old disks that have been stored in non-favourable conditions. 
Due to problems I have had with 5.25” disks failing when I was restoring my Sord computer I decided not to risk them and copied the images to more modern and more reliable 3.5” disks.
 
There are a few modern single board 6809 designs out there that can run Flex but I wanted to build a computer as similar to my original computer as I could thus the SS50 and SS30 boards are all based on old designs using old chips(some of which are only available on Aliexpress or Ebay) this also makes sure it is 100% compatible with the software disks I had, and to add to the vintage computer experience.

The original computer I built used 0.1” pinheader connectors on the boards, however I found the molex connectors that SWTPC used on its SS50 backplanes are still for sale at Mouser and other suppliers in 2025, so I decided to build a mainboard somewhat based on the SWPC MB2. This also means the SS50 and SS30 boards I have made should work in any machine using this bus, (not tested though!)
To make it more user friendly (and make building a case easier) I decided on a ATX form-factor and the option of using a ATX power supply, note: this requires all the voltage regulators on the mainboard & SS50/30 cards to be bridged out. 
The mainboard will bolt into a ATX case though depending on the case used the use of a PicoATX psu (like the one in the photos) may be required to allow more space for SS50 boards.

The cards are designed to use PC card brackets which line up with the slots in the ATX case, or the chassis from Aliexpress that I used. 
The rear connectors use the IBM pinouts to make life easier. (9 & 25-pin Serial ports, 25-pin printer port, 37-pin floppy drive port).

The first boards I made were the minimum needed to get something up and running, the mainboard, cpu card, ram card, and serial card.
Once assembled I was presented with a computer that did nothing! There was no attempt to access the serial card and not much activity on the data bus. 
I made a cut down monitor eprom to try and work out where the problem might be but that didn't run either, which didn't really help. 

After seeing that the CPU was actually doing “something” I decided the no go situation was probably caused by the Ram board.  I decided the way to check this was to design a Parallel Port board with LEDs on it that could display the status of a Ram checking program. 
After the board was made a program was written that used no stack or ram and could be substituted for the Monitor Rom, it tested a predefined memory range displaying progress and errors on the 8-bit LED port. 

It turned out that the ram board had 2 problems! A data buffer enable decoding error AND a data buffer direction selection error.  I must have been half asleep when designing this board!
After bodging a repair the ram test passed, I then fitted the Sbug monitor and I had a monitor prompt on the screen!

The next step was to build a disk controller, some of the disks I had were double density so I used a WD2797 (the same as in my 1980s version). These are quite hard to find and expensive, I found some on Ebay and Aliexpress and bought the cheapest one hoping it would be ok.
When the PCB arrived I assembled it and to my surprise with the Test jumper fitted it put out the correct test signals for calibration.
After calibration I made a cable to connect a pair of 720k drives and tested that the drive was activated when booting with the U command. 
Next the big test I had been waiting for for about a year since starting the project......... with a sssd 35track system disk image I had made from the 40+ year old system disk in the drive, it booted Flex!!

The next task will be to produce a set of disks and images in both 3.5” and 5.25” formats.
Back in the 80's disks were quite expensive so the 30+ disks I have contain a mixture of programs and data that need sorting onto a more logical set of program and data disks, once done I will add them to this repository.





