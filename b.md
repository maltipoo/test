## Program 1 Writeup 
This particular set of data is a simple table with fixed rows and columns.  This means that every object in the json file will have identical fields.  So we really only need to read the field names once, rather than looking for them over and over as we would have to if we were converting from yaml or xml.  So the sql or csv files look like the best options.  The csv file does not contain the field names, but reading the csv file is easier because we do not have to ignore instructions as we would with the sql file.  So converting the csv file looks like the easiest, most efficient option, assuming we already know the field names.

I used Python to write the script.  Here's how it works:  
1. Read a line  
2. Remove quotes and whitespace  
3. Split the line by commas  
4. Write each field name to the json file, followed by the element of the array that matches it, referred to by index.  Each line will be a json object.  
5. Repeat this for the entire file.  
This is simple enough that a number of languages would probably work pretty well.  Python may have good libraries for this sort of thing, but that is irrelevant since we are not using them for this assignment.

| type | size  | zip  | ratio | gzip | ratio |
|------|-------|------|-------|------|-------|
| csv  | 484MB | 51MB |  90%  |
| sql  | 467MB | 52MB |  89%  |
| xml  | 2.3GB | 82MB |  96%  |
| yml  | 771MB | 52MB |  93%  |
