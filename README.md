# Laboratorio-8-0x

Main console display active (Tcl8.5.6 / Tk8.5.6)
(VMD) 1 % help
For help, type help and the name of a topic from the following list:
raster3d   http://www.bmsc.washington.edu/raster3d/
msms       http://www.scripps.edu/pub/olson-web/people/sanner/html/msms_home.html
faq        http://www.ks.uiuc.edu/Research/vmd/allversions/vmd_faq.html
biocore    http://www.ks.uiuc.edu/Research/biocore/
tachyon    http://www.photonlimited.com/~johns/tachyon/
babel      http://www.eyesopen.com/babel/
homepage   http://www.ks.uiuc.edu/Research/vmd/
quickhelp  http://www.ks.uiuc.edu/Research/vmd/vmd_help.html
radiance   http://radsite.lbl.gov/radiance/HOME.html
maillist   http://www.ks.uiuc.edu/Research/vmd/mailing_list/
scripts    http://www.ks.uiuc.edu/Research/vmd/script_library/
namd       http://www.ks.uiuc.edu/Research/namd/
vrml       http://www.web3d.org/
rayshade   http://www-graphics.stanford.edu/~cek/rayshade/rayshade.html
povray     http://www.povray.org/
python     http://www.python.org/
plugins    http://www.ks.uiuc.edu/Research/vmd/plugins/
software   http://www.ks.uiuc.edu/Research/vmd/allversions/related_programs.html
tcl        http://www.tcl.tk/
tutorial   http://www.ks.uiuc.edu/Research/vmd/vmd-1.9.3/docs.html#tutorials
userguide  http://www.ks.uiuc.edu/Research/vmd/vmd-1.9.3/ug/ug.html

>Main< (VMD) 2 % set all[atomselect 0 "protein and resid 230 to 350"]
can't read "allatomselect2": no such variable
>Main< (VMD) 3 % 2
2
>Main< (VMD) 4 % 
>Main< (VMD) 4 % 2
2
>Main< (VMD) 5 % measure center $neko
can't read "neko": no such variable
>Main< (VMD) 6 % measure center$gato
can't read "gato": no such variable
>Main< (VMD) 7 %  measure center $gato
can't read "gato": no such variable
>Main< (VMD) 8 % measure center $set all
can't read "set": no such variable
>Main< (VMD) 9 % 
>Main< (VMD) 9 % set all[atomselect 1 "protein and resid 230 to 250"]
can't read "allatomselect3": no such variable
>Main< (VMD) 10 % set gato [atomselect 1 "protein and resid 230 to 250"]
atomselect4
>Main< (VMD) 11 % measure center $gato
19.23552131652832 -42.01963806152344 -12.19515323638916
>Main< (VMD) 12 % measure minmax $gato
{9.098999977111816 -56.18199920654297 -24.64299964904785} {26.27199935913086 -28.45199966430664 -0.2770000100135803}
>Main< (VMD) 13 % eval vecadd [$gato get charge]
0.0
>Main< (VMD) 14 % set lailara [atomselect 0 "protein and resid 72 to 99"]
atomselect5
>Main< (VMD) 15 % measure mimax $lailara
Type 'measure' for summary of usage

>Main< (VMD) 16 % eval vecadd [$all get charge]
can't read "all": no such variable
>Main< (VMD) 17 % eval vecadd [$lailara get charge]
0.0
>Main< (VMD) 18 % measure minmax $laira
can't read "laira": no such variable
>Main< (VMD) 19 % measure minmax $lailara 
{-20.533000946044922 -16.20800018310547 -16.91200065612793} {22.48200035095215 11.418000221252441 16.139999389648438}
>Main< (VMD) 20 % $lailara [vecinvert [measure center $lailara]]
atomselection: improper method: -3.0568253993988037 0.5450349450111389 -0.6903995871543884
usage: <atomselection> <command> [args...]

Commands for manipulating atomselection metadata:
  frame [new frame value]      -- get/set frame
  molid|molindex               -- get selection's molecule id
  text                         -- get selection's text
  delete                       -- delete atomselection (to free memory)
  global                       -- move atomselection to global scope
  update                       -- recalculate selection

Commands for getting/setting attributes:
  num                          -- number of atoms
  list                         -- get atom indices
  get <list of attributes>     -- for attributes use 'atomselect keywords'
  set <list of attributes> <nested list of values>
  getbonds                     -- get list of bonded atoms
  setbonds <bondlists>
  getbondorders                -- get list of bond orders
  setbondorders <bondlists>
  getbondtypes                 -- get list of bond types
  setbondtypes  <bondlists>
  moveto|moveby <3 vector>     -- change atomic coordinates
  lmoveto|lmoveby <x> <y> <z>
  move <4x4 transforamtion matrix>

Commands for writing to a file:
  writepdb <filename>          -- write sel to PDB file
  writeXXX <filename>          -- write sel to XXX file (if XXX is a known format)

>Main< (VMD) 21 % $lailara moveby [vecinvert [measure center $lailara]]
>Main< (VMD) 22 % set gato [atomselect 1 "all"]
atomselect6
>Main< (VMD) 23 % $gato moveby [vecinvert [measure center $gato]]
>Main< (VMD) 24 % 
>Main< (VMD) 24 % $gato writepdb CENTRADO_3CKZ.pdb
>Main< (VMD) 25 % 
>Main< (VMD) 25 % 
>Main< (VMD) 25 % set gato [atomselect 0 "chain A and name CA and 72 to 98"]
atomselect: cannot parse selection text: chain A and name CA and 72 to 98
>Main< (VMD) 26 % set gato [atomselect 0 "chain A and name CA and resid 72 to 99"]
atomselect7
>Main< (VMD) 27 % set gato [atomselect 0 "chain A and name CA and resid 75 to 85"]
atomselect8
>Main< (VMD) 28 % set lailara [atomselect 1 "name CA and reside 235 to 245"]
atomselect: cannot parse selection text: name CA and reside 235 to 245
>Main< (VMD) 29 % set lailara [atomselect 1 "name CA and resid 235 to 245"]
atomselect9
>Main< (VMD) 30 % measure rmsd $gato $lailara 
17.002490997314453
>Main< (VMD) 31 % 
