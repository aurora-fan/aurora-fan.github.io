---
layout: page
title: Our Progress
icon: fa-tasks
permalink: /our-progress/
order: 3
---

Here you can see all the progress we've made, as well as what's to come! <br /> This page will be updated periodically, but if you want the most up-to-date version, please check out [our Trello](https://trello.com/b/xxT0K6fK/aurora-fan-to-do "Our Trello"). 

### Here's what we've done so far: <br />
Our [blog](/blog/ "Our Blog") is more in-depth source of this information!
* Post to the website each week
    * We've done a post on every Friday since the 7th of November.
    * Each post has a comprehensive breakdown of all our progress that week.
* Made a [Trello](https://trello.com/b/xxT0K6fK/aurora-fan-to-do "Our Trello") to organize our ideas.
    * Our Trello is kept up-to-date in real time, and is public.
    * Contains completed tasks, and WIP tasks.
* Picked-up/Purchased additional parts
    * Bought screws and plywood from The Home Depot.
* Designed our plans for laser-cutting
    * We mapped out the correct measurements on each piece to ensure precision.
* Laser-cut our parts
    * We went down to Mount Holyoke and cut our parts.
    * Our completed pieces have been assembled into our current product.
* Fitted the Hall-Effect Sensor
    * Current main source of RPM calculation.
    * Magnets on fan blades work with sensor at base.
* Worked with our LEDs
    * Soldered the LEDs together.
    * Affixed the LEDs to the fan blades.
* Wrote foundational code
    * We wrote code for the basic functionality of the display.
    * RPM modulation has been integrated.

### Here's what we're still working on: <br />
* Hard-Coding letters (~4 hours)
  * We've decided to hard-code the letters, in order to make more creative demos.
* Fitting LDR or IR Receiver/Transmitter (~6 hours)
  * We're moving towards a new medium for tracking RPM, one that will hopefully be more accurate.
  * We hope to have a transmitter on the opposite side of the blades, and a receiver at the base for tracking RPM.
* Fan Simulator (~12 hours)
  * We're hoping to make a small program that will be able to show what the fan display should show, given an image or selection of specific pixels.
* Weather Display (~6 hours)
  * A weather demo that pulls from a weather database to show the current weather (as well as a small graphic).
* Picture-to-Display (~12 hours)
  * We're planning on writing a compression algorithm to translate small-scale images onto the display.
  * We hope to have this interface with the fan simulator, which should show what the image will look like on the fan itself.
* Music Visualizer (~5 hours)
  * We want to make a demo of a music visualizer, one that shows a small animation involving the amplitude, overall loudness, and frequency of a song playing.
* Start-Up Animation (~4 hours)
  * A small start-up animation we hope to make, just to add that final layer of polish to our project.
  * Perhaps something that displays our name, or simply a small animation would be nice.
* Final Calibrations (~12 hours)
  * Our final calibrations to ensure our project is in the best possible state for oue presentation. 
  * Would involve ensuring our RPM calculation works correctly, and our demos function to the degree we're looking for.

### Roadblocks
Although there is so much done, there's still much to do, and we've faced our fair share of roadblocks:
1. _We've had to restart how we're working with RPM several times_:
  <br />We've gone from trying to maintain a consistent RPM using a MOSFET to using a Hall-Effect sensor to track RPM to LDRs and have even considered using IR receivers and transmitters to keep track of RPM in real time.
1. _We had many problems with laser cutting_:
  <br />We used a different software for creating our pieces for laser cutting and exported as an svg... Only to find out that the laser cutter isn't compatible with svg, unlike most major laser-cutting brands. Suffice to say, we spent many hours amending this issue (costing us both time and money for the rental car!).
1. _Physically limiting hardware_:
  <br /> The slip ring we have has constant electric noise at well below its rated RPM (not to mention it isn't the best slip ring we could be using, a through bore slip ring would be better, but it's much more expensive), <br />the motor doesn't spin at a constant RPM, the neopixel website lists the measurements for the neopixel strips we ordered incorrectly (leading to faulty measurements on our fan blades), we ordered a new slip ring and it arrived broken, and our overall image quality and frame-rate has been severely limited from our original plan, due to the combination of all above issues.
  Overall, we've had the most limitations due to the hardware, but such is the nature of building a product like ours from scratch.

### Lessons Learned & Tips
Despite our struggles, this has still been a learning experience for us both:
1. _Soldering_
  <br />Personally I've spent a lot of time soldering pieces for this project, and i've learned some pretty good techniques for quick and efficient soldering!
  <br />For example, bridging solder across two horizontal pads can be achieved using a small piece of wire and some steady hands! 
1. _Cartesian to polar conversion_
  <br />Although cartesian to polar conversion is something we've both learned in previous classes, actually implementing it in a real-life scenario is something quite different! We were surprised to find how much more it made sense in practice! Applying an idea is one of the best ways to reinforce it in one's mind, so using polar for our calculations has both made our algorithms easier to code-up, and has served as quite the learning experience as well!
1. _Working with ESP32_
  <br />Working with ESP32 has been quite the experience! It's interesting how much one can do with such a small piece of hardware, but it seems that the sky's the limit! Although we've run into a couple of problems due to the limited ability of our particular arduino, we've still managed to get quite a bit of use out of it! We plan (as of writing this) to use it on our final product, and we hope that it's versatility will help us greatly in the long run! 
1. _Github pages/Markdown_
  <br />Using Github pages and Markdown, although not connected to our project specifically (besides through this website), has been quite the learning experience for me personally! Prior to this, I had minimal experience with HTML and website building, but now I feel as though I have a lot more in terms of possibilities for conveying my thoughts/ideas! More so, I feel like I know more about Github as a whole, which is a very popular medium for my major!

### Major Changes
Although documented throughout this page, as well as our blogs, here are some of our most major changes throughout our project:
1. _Constant RPM to tracking RPM dynamically_
  <br />We've had to move towards tracking RPM in real-time, from our original plan of rotating at a constant RPM. This is gone into more detail above and in our blog posts, but the change is mostly due to hardware limitations for both the motor, and the slip ring. 
1. _Solid 30 FPS down to a consistent 5 FPS_
  <br />Originally we had big plans for the display in terms of moving images (likely gifs) and high framerates, however due to a combination of the method of data transfer, the processing power of our Arduino, the communication frequency of the neopixels, the rating of the slip ring (as well as quality) and the max RPM of the motor, we are unable to meet a solid 30 FPS, and have instead decided to focus more on what we can do with what we have.
1. _Hall-Effect to IR Transmitter/Receiver_
  <br />We've gone to-and-from a couple of different sensors for keeping track of RPM, and although Hall-Effect has been the most stable, we still have a long way to go in order to produce a still image on the blades. Currently we're looking at using either a LDR or IR receivers/transmitters, with a priority on the latter. We hope this will help us finalize the RPM calculations so we can make a stable image! 

It's quite interesting to reflect back on our [original presentation](https://docs.google.com/presentation/d/17ro3u3oZ8lFYC3w88OtpE69kU2mOrf_581_JR-Ly-18/edit?usp=sharing "NeoPixel Display") to see some of the changes we've had to make...
<br />We were quite ambitious at the start! But we're still confidant we can refine AuroraFan into a product that we're proud of!