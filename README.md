# Project_Save_the_Plants_WWDC 

Over 18 million Australians have bought some type of indoor plant (Hes D et.al., pg.1, 2019). A study by Hes D et.al. interviewed over 1000 Australians. 40% struggled to know when to water their plants, with 27% struggling to understand why their plants died. A study by Dan and Rae (owners of Terrarium Tribe) concluded that almost all causes of plant death were a result of not watering properly. 

My project aims to ensure that house plants are adequately taken care of. The basis of my project is to use Python as the coding language and Micro:bit as the computing space. The aim is simple: to let users know when to water their plants to prevent them from dying. 

You will find that my code has explored the moisture levels for 1 plant, known as the Peace Lily. However, for future purposes that expand beyond the prototype, this code would include the moisture levels of other plants. 

# Table of Contents
* [Technologies](#technologies)
* [Setup](#setup)
* [Usage](#usage)
* [Extra Notes](#extra-notes)
* [References](#references)


## Technologies

I used multiple tools to complete this project. 

1- Original version of the BBC micro:bit, or known as V1 of the micro:bit 

2- Duinotech Arduino Compatible Soil Moisture Sensor Module - Also compatible with Micro:bit 

Link - https://www.jaycar.com.au/duinotech-arduino-compatible-soil-moisture-sensor-module/p/XC4604 

3- Jumper Leads - Alligator to Pin 

Link - https://www.jaycar.com.au/10-piece-jumper-lead-set-alligator-clip-to-pin/p/WC6032

4- socket to socket jumper lead 

Link - https://www.jaycar.com.au/150mm-socket-to-socket-jumper-leads-40-piece/p/WC6026

5- Peace Lily 

6- MicroPython 

Link - https://microbit-micropython.readthedocs.io/en/latest/tutorials/introduction.html

## Setup

To set up the Device and circuit in sync with the code: 

1. To set up the overall device, you will need to connect the Soil Moisture Sensor Module with a socket-to-socket jumper lead. 
2. Using 3 different pins->Alligator Clips connect the pin to the socket-to-socket jumper lead. 
3. Connect the Alligator Clips to Pin 1, 3.3V and GND.
   a. This will ensure that data is being received on the micro:bit, that the external device is powered (the Soil Monitor in this case) and the GND pin will ensure that the circuit is complete
4. Insert the Soil Monitor into the plant with all wires connected
5. Upload the code into the micro:bit via computer
6. After ejecting the micro:bit from the computer, attach the battery pack
7. Follow any prompts to ensure the conditions of the plant are met

 To make sure the values being inputted to the computer are correct:
 1. Before inserting into the plant, find the reading for complete moisture.
    a. To do this, insert the following code and place the sensor into a glass of water (this is the total moisture level and will be taken out of the final bit of code)  
    from microbit import *

   while True:
    # Read the analog value from pin 1 (returns 0-1023)
   
    analog_value = pin1.read_analog()
   
    # Display the value on the micro:bit's LED screen
    
    display.show(str(analog_value))
    
    sleep(100) # Wait for 100 milliseconds before reading again
   
    # This is to determine the total moisture level, which will read between 0-1023 as the micro:bit has a 10-bit ADC and resolution. 
 
  2. Take the value shown by the LED sensor and find your Min and Max values for moisture. 

a. For the Peace Lily, the ideal conditions would be 50%-60% moisture level. 
    
b. My reading came back as 600 for a 100% Moisture level, so 60% of 600 is 480 (determining my Max condition), and 50% would be 300 (determining the Min condition). 

  3. Using the now known Min and Max values, continue with the code or adjust percentages as determined by the chosen plant.

## Usage

This project is used for the Houseplant owner who does not have a "Green Thumb" and consistently thinks about why the plants they purchase continue to die, or for a curious user who wants the effort taken out of when to water their plant or leave it be. 

This project is versatile for different programmers and users, as it leaves room for different plants to be used or conditions to be monitored (if the right sensor has been found). 
It opens a door for those wanting to reduce waste in the form of plants and organic matter, whilst potentially fulfilling a hobby. 

## Extra Notes

This project is a friendly way to step into the world of plant monitoring. This project can be done with different sensors, plants, and the ability is designed for a user who is just starting and hoping for a challenge!

Please note to reset the firmware to ensure that micro:bit has the most updated firmware to improve function and to be able to upload code. 

All references used for this project have been listed below; most functions and code written were used through the references page, which allowed prompts and tutorials on how to ensure the code was done correctly on the micro:bit. 

## References


ADC and Resolution - SPECTRUM Instrumentation. (2025). *Spectrum-Instrumentation.com*. https://spectrum-instrumentation.com/support/knowledgebase/hardware_features/ADC_and_Resolution.php

Analog Read Pin. (2022). *Microsoft MakeCode*. https://makecode.microbit.org/reference/pins/analog-read-pin#:~:text=Example,number%20on%20the%20LED%20screen.&text=If%20you%20are%20using%20analog,between%20the%20two%20micro:bits.

BBC micro:bit overview. (2025). *Microbit.org*. https://microbit.org/get-started/features/overview/#:~:text=The%20GND%20pin%20is%20the,switches%20to%20your%20micro:bit.

Code. (2020). *Microsoft MakeCode*. https://makecode.microbit.org/projects/soil-moisture/code

Gokhale, S. (2023, April 21). How to print a percentage value in Python? *AskPython*. https://www.askpython.com/python/examples/print-a-percentage-value-in-python

Greener Spaces Better Places. (2019). Plant Life Balance trend report 2020. https://home.greenerspacesbetterplaces.com.au/wp-content/uploads/2019/12/PLBTrendReport_2020.pdf

Hardware. (2025). *Microbit.org*. https://tech.microbit.org/hardware/

Images — BBC micro:bit MicroPython 1.1.1 documentation. (2015). Readthedocs.io. https://microbit-micropython.readthedocs.io/en/latest/tutorials/images.html

Introduction — BBC micro:bit MicroPython 1.1.1 documentation. (2015). *Readthedocs.io*. https://microbit-micropython.readthedocs.io/en/latest/tutorials/introduction.html

Linkedin.com. (2025). *Python for Students*. https://www.linkedin.com/learning/python-for-students-2023/python-for-students?u=2129308

Łyczywek, R. (2018, October 15). How to write a good README for your GitHub project? *Bulldogjob.com*. https://bulldogjob.com/readme/how-to-write-a-good-readme-for-your-github-project

Make. (2020). *Microsoft MakeCode*. https://makecode.microbit.org/projects/soil-moisture/make

micro:bit firmware. (2025). *Microbit.org*. https://microbit.org/get-started/user-guide/firmware/?_gl=1*4o18p9*mb_ga*MjExNTAzMzYwMi4xNzU3NDAzMDAy*mb_ga_FE3HZ3W83X*czE3NjE3MDU4ODAkbzEyJGcxJHQxNzYxNzA3MjE0JGo0OSRsMCRoMA..

Peace Lily (Spathiphyllum). (2023). *Gardenia*. https://www.gardenia.net/plant/peace-lily-spathiphyllum#:~:text=Light:%20bright%2C%20indirect;%20tolerates,for%20vigorous%20peace%20lily%20growth.

Soltech. (2025). *Peace Lily*. https://soltech.com/products/peace-lily-care#:~:text=The%20pH%20of%20the%20soil,lot%20of%20air%20in%20it.

Terrarium Tribe. (n.d.). Houseplant statistics. https://terrariumtribe.com/houseplant-statistics/

The Sill. (n.d.). Why plant leaves turn yellow. https://www.thesill.com/blogs/care-miscellaneous/why-plant-leaves-turn-yellow
‌
