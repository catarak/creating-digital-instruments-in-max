# Creating Digital Instruments in Max

## Authors
Cassie Tarakajian, Ashley Bellouin 

## Before we start...
- What is a musical instrument?
- Who makes music instruments?
- What are some barriers to creating music?
- What is the most recently invented instrument?

## Introduction
This workshop will focus on using Max software to create custom digital musical instruments. Starting from a beginners standpoint, we will introduce Max and cover the basics of the software, then focus on creating experimental sounds by manipulating provided audio recordings and/or student’s own recordings. Some processing techniques that will be covered are delay, feedback, and filtering, as well as how to create a simple vocoder and sequencer. We will also show how to interact with these programs through a simple, custom interface. At the end of the workshop, students should understand how to create their own digital musical instruments that can be played by anyone. By creating a final interface that is simple to understand and interact with, these digital instruments become accessible to the vast majority of people. No musical or programming knowledge is required to create sound. In general, classical musical instruments have complex designs that can be intimidating to approach, require certain physicality to use, and take years of practice to understand. The end goal of this workshop is to create a musical instrument that anyone can play through a few simple button presses.

### Target Audience / Prerequisite & Pre-Assessment
High school students, ages 14+. No prerequisites required. Please have Max 8 and Audacity installed on your machine before the start of class. If there are specific sound samples you want to use in the workshop, please download and bring them to class. You can search for free sounds here: https://freesound.org/

### Outcomes & Goals
In this workshop we will be creating custom digital musical instruments using Max software and audio recordings. Students will walk away with a deeper understanding of digital audio and how to build a few different types of digital instruments. They will also learn about different types of musical interfaces.

### Pacing / Duration
4 hours total
#### Part 1: 2 hours
* ~30 min - Introduction to Workshop. 
  * What is a musical instrument? 
  * What is Max and what can you do with it? Show example works.
  * Get acquainted with the Max interface
* ~50 min - The basics of manipulating a sound 
  * How to play back a sound file
  * Adjust speed, switch between files
  * Feedback
  * Delay
  * Filtering 
  * Presets 
  * Audacity (if time permits)
* ~10 min - Break
* ~30 min - Sequencer
  * What is a sequencer? 
  * metro, cycle, ggate
  
#### Part 2: 2 hours
* ~30 min - Vocoder 
  * What is a vocoder?
  * Show examples built into Max. Copy/paste from example patch. 
  * Panning
* ~40 min - Integrate a controller/Create custom interface
  * Look at examples of different musical interfaces.
  * What are different ways you can trigger or control your patch? 
   * Use your keyboard as a controller
   * Trigger events through audio input 
  * Presentation mode 
* ~5 min - Break
* ~45 min - Group Projects
  * Working in groups of 2, make a patch that incorporates techniques from the first and second parts of the workshop. Control some aspect of your patch with either audio input or your keyboard, and create a user interface in presentation mode that anyone can understand. 

## Materials Needed & Exercises To Do Before Class
### Software to download ahead of time
* [Max 8](https://cycling74.com/products/max-features) from Cycling '74
* [Audacity](https://www.audacityteam.org/)

### Materials and Resources
* Please download this folder before class and place it in your Documents folder: https://cycling74.s3.amazonaws.com/support/Eyebeam_Max.zip
* If you want, you can download more free sounds from here: https://freesound.org/

### Vocabulary
* DAW (Digital Audio Workstation): Software used for recording, editing, and producing audio files
* Patch: This refers to the programs that you create in Max.
* Digital Instrument: an instrument composed of hardware, software, and a user interface.
* Audio Effect: a way to change the characteristics of a sound. 
* Vocoder: a synthesizer that produces sounds from an analysis of audio input. This was originally used for a voice effect. 
* Sequencer: a system for outputting events (sounds) at specified intervals.
* Delay: an audio effect that records an input signal, then plays it back after a period of time.
* Feedback: A signal chain where the output of a signal is fed back into it's input. 
* Filtering: an audio effect that heightens or lowers certain frequencies in a sound. 
* Program: A procedure, or set of instructions, that performs a specific task when executed by a computer. 
* Programming Language: The human-readable commands and syntax (or grammar rules) used to write programs. 
* Graphical Programming Language: A programming language in which users create programs by manipulating elements using a GUI (graphical user interface) rather than using text. 

### Listening & Watching Examples
* [Lucky Dragons - Make a Baby](https://luckydragons.org/category/make-a-baby/)
* [The Instruments of Laetitia Sonami](http://sonami.net/instruments/)
* [Leafcutter John - Against the Clock](https://www.youtube.com/watch?v=X1cmWFP3f8o)
* [Tarik Barri and Sote - Sacred Horror in Design](https://vimeo.com/244348082)
* [Interview with Jessica Ekomane](https://cycling74.com/articles/artist-focus-jessica-ekomane)
* [Interview with AGF](https://cycling74.com/articles/an-interview-with-antye-greie-ripatti-agf)
* [Radiohead - The Gloaming](https://www.youtube.com/watch?v=l05EBdxKo2U)

## Exercise Descriptions
* The basics of manipulating a sound (50 minutes)
  * Show how to play back a sound file using buffer~ and groove~. Copy/paste from the groove~ help patch! Show that all help patches are interactive. 
  * Introduce proper naming techniques, file preferences 
  * Looping, adjust speed, timestretch, switch between files (umenu)
  * Delay/Feedback - tapin~ and tapout~. Show how to encapsulate.
  * Filtering - biquad~ with a filtergraph~. Copy/paste from the biquad~ help patch. Go over the main filter types.
  * Save presets with the preset object. Some objects, such as attrui, cannot be saved with presets. Change these to a umenu.
  * If there's extra time, show how to record in Audacity and export. These files can then be loaded into Max.
* Sequencer (30 minutes)
  * Explain what a sequencer is. 
  * Make a simple sequencer by triggering different groove~ objects to play sound files. 
  * Use metro, cycle, and ggate. You can skip a step in the sequence by "closing" the ggate.  
  * Add presets 
* Vocoder (30 minutes)
  * Explain what a vocoder is. 
  * Show the example built into Max. Extras > Examples Overview > MSP > Effects.
  * Copy/paste from example patch into your own patch. When copying a section from a different patch, pay attention to where that section goes in the signal chain. 
  * Panning with pan2S. Use a cycle~ object to control panning speed. 
  * You can have two separate channels where you process the audio differently, then pan those channels to be out of phase with each other. 
* Integrate a controller/Create custom interface (40 minutes) 
  * Look at examples of different musical interfaces: Buchla, Theramin, Lucky Dragons, Laetitia Sonami, etc. 
  * What are different ways you can trigger or control your patch? 
   * Use your keyboard as a controller - key and sel objects. Introduce random and scale objects.      
   * Trigger events through audio input - adc~, peakamp~ and if/then to trigger based on amplitude. 
  * Presentation mode - clean up your patch into a nice presentation so that anyone can approach it and make sound. 
* Group Projects (45 minutes) 
  * Working in groups of 2, make a patch that incorporates techniques from the first and second parts of the workshop. Experiment with all the different types of sounds you can make. Write down what you did. Control some aspect of your patch with either audio input or your keyboard, and create a user interface in presentation mode that anyone can understand. At the end of class be ready to explain what you did and why. 

## Student Reflections, Takeaways and Next Steps
You can continue learning Max with these Resources:
* [Programming Max: Structuring Interactive Software for Digital Arts (Kadenze Course)](https://www.kadenze.com/courses/programming-max-structuring-interactive-software-for-digital-arts/info)
* [Delicious Max Tutorials](https://www.youtube.com/user/dude837)
* [Max/MSP/Jitter for Music](https://amazon.com/Max-MSP-Jitter-Music-Interactive/dp/0190243740/ref=dp_ob_title_bk)
* [20 Objects](http://darwingrosse.com/20Objects/)
* [Max 8 Tutorials (by dearjohnreed)](https://www.youtube.com/playlist?list=PLVIa8UkRzErsL95NoKH0QFaoLVMFqxbnA)
* We also recommend looking into Max For Live and Ableton Live as companion tools

Need help with your patch? Our online forums are a great way to get help from fellow Max users: https://cycling74.com/forums

If you would like to share the work you have created with Max, you can submit a project on Cycling 74's website: https://cycling74.com/projects

## Post Session

### References
* [Cycling 74](www.cycling74.com) 
* [Audacity](https://www.audacityteam.org/)
* [Free Sound](https://freesound.org/)

### Implementation Guidance &  Teaching Reflection  
* The main goal of this course should be to have fun and inspire the students! Attention spans can quickly diminish if too much time is spent instructing. Instead of lecturing, make sure students quickly start creating patches. 
* Students learn better when they make their own patches, instead of playing with pre-built ones. Have them patch along in the beginning, then make sure to have dedicated lab time where they can create their own work. 
* A lot of class time can be wasted on finding audio samples online. Provide a curated selection of samples that they can work with. Make sure these samples sound good when processed using the techniques taught. Have nature sounds, classic instruments, percussion, and some more experimental sounds. 
