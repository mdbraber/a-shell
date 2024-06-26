﻿The location of source files for Serbian spelling dictionary were downloaded
from 
https://github.com/LibreOffice/dictionaries/tree/master/sr
(Serbian Spelling and Hyphenation for LibreOffice).

Here is the content of original README file from the repository:

	"LibreOffice Spelling and Hyphenation
	extension package for Serbian (Cyrillic and Latin)
	
	This extension package includes the Hunspell dictionary and Hyphen
	hyphenation patterns for the Serbian language adapted for usage in
	LibreOffice.
	
	Serbian spelling dictionary is developed by Milutin Smiljanic
	<msmiljanic.gm@gmail.com> and is released under GNU LGPL version 3 or
	later / MPL version 2 or later / GNU GPL version 3 or later, giving
	you the choice of one of the three sets of free software licensing
	terms.
	
	Serbian hyphenation patterns are derived from the official TeX
	patterns for Serbocroatian language (Cyrillic and Latin) created by
	Dejan Muhamedagić, version 2.02 from 22 June 2008 adopted for usage
	with Hyphen hyphenation library and released under GNU LGPL version
	2.1 or later."


This dictionary used to create Vim spl file is the result of merging the two
LibreOffice dictionaries, for cyrillic and latin script.

The merge was accomplished by concatenating two .dic files, removing 1061
duplicates using the fixdup Vim script and updating the word count.

In both affix files each SFX (and two PFX) directive had to be appended with
the . at the end of the line. KEY and WORDCHAR directives were removed, and
MIDWORD was added.  Each SFX block is the union of corresponding blocks from
sr.aff and sr-Latn.aff.  Header line of each block was updated to the new
count (2 times the value from the corresponding block in the input affix
file).


Ivan Pešić
23.06.2022. 
