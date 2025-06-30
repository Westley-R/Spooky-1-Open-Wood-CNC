---
title: "Spooky 1: Open Wood CNC"
author: "Westley R"
description: "An open source wood CNC platform that supports anything from laser cutting to CNC milling"
created_at: "2025-06-27"
---

# June 30th: And so the madness begins

I started to get the PCB put together, and just about as fast as I decided on the Raspberry Pi Pico, I decided against it. The PCB still has the Pico wired into it, but towards the end of my work today, I realized that the Pico doesn't have nearly enough UART ports. The Pico only supports 2 UART ports despite having 5 UART pin pairs. 

So far, I've gotten the steppers and a voltage regulator wired up, although I still need to add resistors and capacitors between a few of the connections.

![No PCB?](Project%20Pictures/PCB%20Progress%20Day%201.png)

I decided on some TMC2209 stepper drivers for their UART and sensorless homing capabilities, as well as a pretty good max output amperage compared to some of the other options. Although I'm designing this PCB around the 2209, it should still be pin compatible with similar boards like the 2208.

Honestly, I spent most of my 1.75h today just looking at pinouts and different voltage regulators. I also found and installed an app called [Activity Watch](https://activitywatch.net), which I'll be using to track my time from now on, as it automatically detects AFK time and ignores it. Activity Watch should make keeping track of my project time a lot easier.

![I installed an activity tracker!](Project%20Pictures/Day%201%20Time%20Sheet.png)

**Total Time Spent: 3.75h**

# June 27th: Started my journey!

Started getting ideas drawn up and putting together some kind of plan for the mainboard. I think I want to take this behemoth of a project one step at a time, and I particularly enjoy the electronics side of projects, so I'm starting on that first. I hope to start on some CAD for the actual machine next week.

During my idea session, I pulled up a few different mainboards and stepper drivers, including the [physect spider 3.0](https://www.fysetc.com/products/pre-sale-fysetc-spider-v1-0-motherboard-32bit-controller-board-tmc2208-tmc2209-3d-printer-part-replace-skr-v1-3-for-voron?variant=39404109267119), which is a great example of an open-source 3d printer mainboard, and a generic [tmc2209](https://www.aliexpress.us/item/3256809113526539.html) off AliExpress.

![Oops! Cannot find the idea board! Did you eat it? Did it ever exist?](Project%20Pictures/Mainboard%20Design%20Idea.jpg)
(P.S. Don't mind my handwriting)

I want to use the Raspberry Pi Pico as the main microcontroller as it is small, fast, and generally pretty power efficient; looking at the pinout I will either have to add an SPI to UART adapter, or switch to a different microcontroller with more UART ports in order to support all of the TMC2209 stepper drivers. 
In addition to just coming up with ideas, I started to work on adding some of the more common PCB footprints and symbols to my design (honestly, just some generic [GPIO headers](https://cdn.sparkfun.com/datasheets/Dev/RaspberryPi/12313.pdf) and [TMC2209 stepper drivers](https://www.aliexpress.us/item/3256809113526539.html)).

**Total Time Spent: 2h**
