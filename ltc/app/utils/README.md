# Python Utils
[stadocgen/utils]  
This folder contains a collection of useful transformation and analysis python scripts 

[stadocgen/utils/transformations]  
Scripts that transform source csv files for purposes of web documentation. The source data is stored under data/source and the target output is stored under data/output

[stadocgen/utils/analysis]  
Scripts to analyze the transformation results

[stadocgen/utils/schemas]
Scripts to generate schemas of source and target csv files

## Workflow
1. Refresh ltc_term_source file using the script in the LtC repository (/utils/refresh_terms_source.py)
2. Run copy_source_files.py to copy the latest source files into StaDocGen
3. Run the script terms_transformations.py to generate the transformed versions of the ltc source files
4. Run the script, sssom_transformations.py to generate the transformed mappings 
3. The output from steps 3 and 4 will be stored under data/output. The website generator only uses data stored in the output directory. 
Therefore, the transformation scripts are required before the documentation pages will show the source data changes.
