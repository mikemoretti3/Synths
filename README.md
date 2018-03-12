This is my synth design repo.  It includes schematics, board files, and notes for some of the synth designs I've made/borrowed.  Some of these come from Electronotes, MFOS, and elsewhere.  There are also my own designs (under the mordent directory).

The files in this repo were made using Eagle 6.5 (and there is a library file I use in here too).

In general, I prefer flying wire panel component wiring.  I have one pad for GNDPNL which I use to ground all my panel components that need ground.  I connect that pad to one component and then string the rest off each other from there.  Also, make note of pot-pinout.jpg.  That is how I wire pretty much all my pots.  Some of the Electronotes ones may be backward (because I messed up the ordering or they just did it in reverse; I've seen this on VCF frequency/resonance pots from different vendors; some turn clockwise for higher resonance, etc and some turn anti-clockwise).

Don't build VCO1.  I have to look at my module and take a picture and figure out some resistor changes.  I probably shouldn't have included that one yet (I plan to redo that board at some point).

The VEWA can be built as separate modules (this is my preferred way to build it).  There is an LFO board and a filter board.  For the filter board I put jacks in for the 3 frequency CVs  (one for each of the formant filters), the notch, and the Q.  This module is wired for +/-15v.  If you have +/-12 look at the jpg for that.  It's ok to use 100k pots instead of 200k.  There are lines marked A though H, only 5 of which have pads, here is what they mean (ignore the fact that they say "to switches" unless you want to combine the lfo board with it):
C,D,E - are input jacks for freq modulation for the 1st-3rd formant  filters
G - is an input jack for the notch filter frequency CV modulation
H - is an input jack for Q (resonance) CV modulation (Q anim),  (internally it's attached to pin 1 of the Q anim pot, this gets fed into the Q summer which outputs to line B)
There are a total of 7 jacks (in, out, and 5 cv modulation inputs).
You can ignore +15VBB, -15VBB, and GNDBB, they were board to board power  for the LFO board that went with the dual board version and aren't connected.  GNDPNL is the ground I use for all the panel wiring and I run ground wires from panel component to panel component.

Most of the rest of the boards are set to run off +/-12v.  +/-15v should be fine although some of the audio signals may be > +/-5v.

The EchoFX is straight from Music From Outer Space; design notes are there.

The Electronotes ones are documented in the EN pdf files.

Under the "mordent" folder, I have my own drum module design based on some electronotes filters, noise, vcos, and ring modulators.  It's very modular and you can probably stripboard or chop out individual parts of it (i.e. noise + filter + env; vco + env; vco + vco + ringmod).  It's pretty straightforward from the board layout and schematic.  There's also a little mixer and mult board.

There's a util-vco that I use a LOT to test new designs with.  I have 12v and 15v versions of this built that I use as a VCO for input to something or an LFO (it has a huge range).  It's not super accurate, but for using it as a test unit it's perfect.

If you have any questions at all please feel free to contact me via github.

Enjoy!
-m
-- 
Mike Moretti
http://mordent.com
♩♫♫♩♪♩
