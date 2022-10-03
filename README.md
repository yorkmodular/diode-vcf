# Diode ladder VCF

Think of this as the bigger, uglier sibling of the MS20-style YAMS filter - it's bigger, badder, squallier and has voltage-controlled resonance too.

It also uses a lot of diodes (14 of them, to be precise)

This is a mostly through-hole build - the surface-mount LM13700 has been pre-soldered for your comfort and convenience.

## Files

You will find the following files here:

* `diode-vcf-schematic.png` - module schematic.
* `diode-vcf-BOM.xlsx` - BOM (Bill Of Materials)
* `diode-vcf-panel.fpd` and `diode-vcf-panel.dxf` - panel files; use these as a base if you wish to create your own, customised panel.

## Build Notes  

The build is relatively straightforward - the surface-mount LM13700 OTA has been pre-soldered. There are no wilfully weird components, but note the following:

* All diodes are 1N4148 or equivalent. Pay attention to their orientation before you solder them in place - the cathode (generally a black stripe) should correspond to the ring on the silkscreen.
* The paired transistors (Q1/Q5 and Q2/Q4) should be in contact with each other - you can either use a small zip-tie, thermal paste or glue for this. Matching the transistors isn't important, but if you want to do that then go nuts.
* The 'main' filter capacitors are C2-C4 - for best results, use polypropylene film caps; you could use ceramics in a pinch but you might need to get creative mounting them. Lower values will lead to 'sharper' resonance; lower than 33nF isn't recommended
* If you want to lessen the effect of the resonance controls, increase the values of R14 and R15 (200k is a good alternative value)
* There are two trimmers on the board - VOCT-TRIM1 controls the V/oct response of the exponential converter (Q1/Q3). CUT-TRIM1 is an offset for the cutoff CV; adjust this until you get a response you like. You probably want to be shooting for 0V at the base of Q1 with both the level and cut pots fully counterclockwise.
* All electrolytic capacitors are 10uF with the exception of C6 (150-220uF) - for best results, use 25V rated caps (50V will also work but these tend to be bulkier)
* All pots are 100k, linear taper.
