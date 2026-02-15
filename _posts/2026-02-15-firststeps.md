---
title: "First Steps"
date: 2026-02-15
---
  
First things first, as much as I want to jump straight into coding away, I need to have a proper analysis of how the different parts of the Gameboy Color work. To better understand the hardware components, I'll be using the [Gameboy PanDocs document](https://gbdev.io/pandocs/), widely regarded as the most comprehensive public technical reference for the Gameboy.

## Understanding the Gameboy
In order to plan out the emulator, it's important to know what components and functions make up the console. 

Inside of a Gameboy Color, there are a couple different processors that I will need to emulate to get games to work:
- An 8 bit Sharp SM83 CPU for the main processor
- A Picture Processing Unit (PPU) capable of rendering a max of 10 sprites per line, or 40 sprites to the screen in 32 768 different colours
- An Audio Processing Unit (APU) to provide audio through 4 channels with stereo output

I'll also need to handle user input, which will not only involve reading the input from the keyboard, but also emulating I/O related hardware interrupts.

![Gameboy Emulator UML Class Diagram]({{ site.baseurl }}/assets/gameboy_emulator_uml_class_diagram.jpg){: width="100%" }
All this so far leaves us with the above diagram as a foundation of sorts for the project. 

