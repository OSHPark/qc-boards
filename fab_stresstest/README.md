# Fab Stresstest

I originally designed these boards as competitive analysis boards,
to test the actual capabilities of other fabs.  

These are interesting because they contain lots of features that
make them deliberately difficult to manufacture, and simple to test
with a small set of test points.

## Built-in Tests and Measurements

The main structure of the board consists of two runs of 6 mil traces,
zigging and zagging, weaving in and out of and around vias, for a
run of over 90 linear inches.

Since the entire board is made of just two signals, any electrical
defects (breaks / shorts), can be detected by measuring continuity
between the points labeled 1 and 2 on the lower left corner of the
board.

* Measure for continuity between 1 and 1 - There should be continuity.
* Measure for continuity between 1 and 2 - There should not be continuity.
* Measure for continuity between 2 and 2 - There should be continuity.

### The main zig-zag loop

This is the back-and-forth structure that makes up more than half
of the board.  Two 6 mil traces follow each other (6 mils apart)
for 70 linear inches.  

There's no mask between the two traces, so lots of opportunities
for shorts due to the plating finish.

I _did_ put mask where the same signal travels parallel to itself.
This provides a test of mask quality and alignment.

There are seventy sharp 90 degree angles which can cause acid traps
and over-etching.

### "Woodpecker Gauntlet"

Just to the right of the main zig-zag loop is a place where the two
traces weave around 29 unplated vias. If the drilling registration
or hole size is off by more than 2.5 mils, then the drilling will hit a
trace. 

### Via Field

In the lower right of the board is the Via Field, where the traces go
through 200 vias.  If any of them aren't plated properly, there could
be a break in the signal.

### More zigging

In the upper right is another zig-zag field.  This was mostly just
space filler, and isn't even as rigorous as the main zig-zag field.

### Mask alignment test

On the back of the board is an extended tic-tac-toe pattern designed to
measure bottom layer mask-to-copper registration.  It doesn't do a great
job, and I've since come up with better ways to do this test.

### Mask webbing test

Labeled "3 4 5 6" in silkscreen on the back is a mask opening test to show
how reliability a fab can do thin openings in the mask (down to 3 mils wide).

### "Regular" and "Vernier"

These sections are designed to measure top-to-bottom copper registration by
cutting the board in half and looking at the board on its edge along the side.

I've never performed this test, and have since thought of better
ways to do it.
