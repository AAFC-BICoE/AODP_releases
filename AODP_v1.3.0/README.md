####README 

#####Automated Oligo Design Pipeline version 1.3.0 (AODP_v1.3.0)
========================================================
DOI: 10.5281/zenodo.10762

Authors: Kaisheng (Kevin) Chen, Chuyang (Charles) Qi, Eric Hardy, Wen Chen* (wen.chen@agr.gc.ca)

The Automated Oligoneucleotide Design Pipeline extracts signature oligonucleotides of specified lengths primarily using the program SigOli (Signature Oligo, Manuel Zahariev 2009). 
Signature oligonucleotides designed for hierarchically clustered taxon groups of interest, can be used 1) to construct DNA arrays for hybridization; or 2) for in silico probing of species with great accuracy from NGS databases.

License:

Copyright (c) 2014 Government of Canada

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


#####Synopsis
--------------
```
	perl AODP.pl [-i] [-n] [-u] [-c CONFIG] [--help]
```

#####Quick start
---------------

1. Download AODP_v1.3.0.tar.gz, reference_databases.tar.gz and AODP_indata_testsets.tar.gz to your local working directory.
2. Start a terminal in Linux platform (e.g. ubuntu virtualbox)
3. Extract archives by using command: tar xvzf filename
4. The newly generated folder AODP_v1.3.0 contains the source codes of main drive program (AODP.pl) and all modules it would call. The folder Reference_databases contains reference databases for cross-validation of oligo specificity. The folder AODP_indata_testsets contains input data for test runs.
5. Place all files in Reference_databases folder in to subfolder Reference within the AODP_v1.3.0 directory; and put all subfolders in AODP_indata_testsets into subfolder indata within the AODP_v1.3.0 directory.
6. Edit config file within the AODP_v1.3.0 directory to suit your need. 
7. Quick usage is listed as follows; further instructions, including detailed descriptions of inputs and outputs, can be found in the user's manual and the perldoc (perldoc AODP.pl).

  * Design signature oligonucleotides for all hierarchical clusters without cross-validation 
```
	perl AODP.pl 
```
  * Design signature oligonucleotides for selected isolates without cross-validation
```
	perl AODP.pl -i
```
  * Design signature oligonucleotides for selected isolates with cross-validation
```
	perl AODP.pl -i -u
```
  * Design signature oligonucleotides for all hierarchical clusters with cross-validation
```
	perl AODP.pl -u
```
  * Use a specific config file
```
	perl AODP.pl [-i] [-n] [-u] [-c /ABSOLUTE/PATH/TO/CONFIG]
```
	


