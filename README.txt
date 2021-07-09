Rosetta Scripts Protocol in two steps:

Step 1: 
strBundle_t1_bgs_hbnet.xml

Generates a 4 helix bundle based on parameters input at command line then search for hyrogen bond networks.
A 'fake' .pdb is required for input since Rosetta Scripts requires a pdb input
Insert tyrosines and phosphosite from .res file
The example here should find networks but will fail to pass the hbnet mover settings. Lowering the cut-offs will allow an output.

Example command line -> replace with your own sampling parameters and change path to rosetta scripts executable

Step 2:

Takes a helical bundle with hydrogen bond networks and add another network at the bottom then design the rest of the sidechains
.res file to keep phospho-site via task operation
.cst file to keep constraints for previous hydrogen bond-network #bug in hbnet, need to uncomment output constraints from ouput cst
.comp file to control aa distribution
 
#Check CRLF versus LF issues if files don't load in Rosetta
