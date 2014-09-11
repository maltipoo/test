### Program 1 Writeup 
I chose to convert the csv file because of the simplicity of parsing it line by line for the fields 
we needed for the json file.  I used Python to read each line, split it into an array (by quotation 
marks instead of commas, to avoid removing quotes later), and then get the three elements (lat, lon,
and time) by their indices, and write them to the json file with the proper labels.
