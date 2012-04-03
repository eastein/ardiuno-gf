Arduino: GF
-----------

Arduino as a hardware platform has grown incredibly over the last few years.
However, Arduino as a software IDE has done nothing but wallow in a mess of
java and horrible text editing. Arduino has developed an almost-c++ language
and has made it impossible to use another IDE or editor besides the almost
useless Arduino IDE because of the way it does internal pre-processing on its
code before passing it along to avr-g++.

You should be able to use vim.  When Arduino-gf is installed, you should be
able to get proper styling in your favorite text editor.

*Let's fucking fix that.*

Arduino-gf is a preprocessor which turns non-portable Processing language in
to nice, shiny C++ which can be compiled using avr-g++ and uploaded to a
device using avrdude.

Basically, we will implement everything that the Arduino IDE does for you in
nice comforting command line.  Well, most everything anyway.  The parts that
you wish you had when you see a .pde file and think "once more into the breach."

Instructions
------------

```arduino-gf''' is a command line tool which has a handful of features that
are not present outside of the Arduino IDE. 

Arduino-GF is best used as part of a standard cmake- or make-based build
chain. Example make and cmake files are included in the examples/ directory.

### Preprocessing #

The biggest problem of developing outside of Arduino is that there is no way
to transition between between Processing and C++ which avr-g++ can eat. 

```arduino-gf $file.pde``` will turn a pre-1.0 Arduino file in to a cpp
which can be then fed in to avr-g++ using your build chain.

```arduino-gf $file.ino``` will turn a 1.0 or newer Arduino file in to a
cpp file which can ben then fed in to avr-g++ using your build chain.

#### Options #

```--out $dir```: output the source files to $dir.



