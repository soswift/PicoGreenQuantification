# PicoGreenQuntification
 Sean Swift 20181211
how to use PicoGreenQuant_in_R.R

# List of inputs

Must include:
-i	= Input, i.e. your fluorescence data as exported from thermal cloud in 'raw data' .csv format

-m	= Metadata, i.e. "Plate#_mapping.csv" spreadsheet, downloaded as a .csv file.
	  If you moved any of your samples around (e.g. moved the first column to the end) this should be reflected in the mapping file.
	  Fluorescence data will be linked with sample metadata based on location on the plate.
	  The script assumes you are putting standards in the first column, concentrations decreasing from well A->H.

-o     = Whatever name you want the output file to have


# What to enter into the command line

 1. Move your input and metadata files into the folder
 i.e. download "Plate#_PicoGreen_Assay" a csv and move it to Desktop/R/PicoGreen_script/
 then download the "Plate#_mapping" .csv from your phone and move it to Desktop/R/PicoGreen_script/

 2. Open terminal
 3. Change the directory so that you are in the CMAIKI_plate_script folder

 cd Desktop/R/PicoGreen_script/

 4. Run ./PicoGreenQuant_in_R.R with input (-i) as fluorescence data .csv and metadata (-m) as the plate mapping file.
 note: these must be in the same folder as PicoGreenQuant_in_R.R, or you will need to specify which folder they are in.

./make_plate_map.r -i "EXAMPLE_INPUT_PicoGreen_Assay_Plate3.csv" -m "EXAMPLE_METADATA_cmaikibarcodes_Plate3.mapping.csv" -o "my_plate_name"

 Ignore any warning, but make sure there are no ERROR messages, because this means things didn't work. 
 Go back and check your spreadsheets to make sure they don't have duplicate entries or missing information.
