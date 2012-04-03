Arduino: GF
-----------

Arduino as a hardware platform has grown incredibly over the last few years.
However, Arduino as a software IDE has done nothing but wallow in a mess of
java and horrible text editing. Arduino has developed an almost-c++ language
and has made it impossible to use another IDE or editor besides the almost
useless Arduino IDE because of the way it does internal pre-processing on its
code before passing it along to avr-g++.

*Let's fucking fix that.*

Arduino-gf is a preprocessor which turns non-portable Processing language in
to nice, shiny C++ which can be compiled using avr-g++ and uploaded to a
device using avrdude.

