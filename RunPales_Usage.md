RunPales v1.0
=============

RunPales reads all the pdbs from a directory, calls Pales to calculate the RDCs and finally parses the Pales generated RDC file to conver it into a numpy array. This array is the input needed for MaxEnt.


##Usage:

`RunPales.py [-h] --path PATH [--outdirectory OUTDIRECTORY]
                   [--outarray OUTARRAY] --inD IND [-H]
                   indirectory`

Extract RDC values from .pdb files using the PALES program.

positional arguments:
  `indirectory`           The directory where the pdbs are.

optional arguments:
  `-h`, `--help`            show this help message and exit
  `--path PATH`, `-p PATH`  The path to the pales executable is.
  `--outdirectory OUTDIRECTORY`, `-outD OUTDIRECTORY`
                        The directory where the RDCs outfiles are going to be.
                        (Default is indirectory)
  `--outarray OUTARRAY`, `-outA OUTARRAY`
                        The name of the file containing the array of RDCs.
                        (Default is rdcs.npy)
  `--inD IND`             Dipolar Coupling input file. Determine which rdcs to
                        calculate (see Pales documpentation).
  `-H`                    Use -H option in Pales (see Pales documentation).



Usage examples:
```
python3 RunPales-1.0.py pdbs --path '/home/melchor/Software/pales/linux/pales' \
--outdirectory 'rdc_files' -inD 'sendai.rdcs' -H
```
Alternatively, after download, you can convert the python file into an executable with:
`chmod +x RunPales-1.0.py`.
Then, you can call it with:
```
RunPales-1.0.py pdbs --path '/home/melchor/Software/pales/linux/pales' \
--outdirectory 'rdc_files' -inD 'sendai.rdcs' -H
```
