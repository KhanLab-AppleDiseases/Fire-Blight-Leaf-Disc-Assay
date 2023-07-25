# Fire Blight Leaf Disc Assay
The image analysis pipeline from the paper "Image-based leaf disc assay for the rapid evaluation of genetic resistance to fire blight in apples" 

(Preprint | https://www.researchsquare.com/article/rs-2829015/v1)

## Basic Usage
Language: Python

This code was written using JupyterNotebook, so it is suggested to continue using IDEs compatible with the .ipynb filetype (i.e. JupyterNotebook, VSCode, etc.)

## Preprocessing
Software: ImageJ (Fiji) 

![image](https://github.com/RichardTegtmeier/Fire-Blight-Leaf-Disc-Assay/assets/55664780/d0ecad09-d52a-4b38-8117-fc6625ad4f90)

**1)** Use the image -> transform options to properly orient the full tray image

**2)** Use the polygon selections + Edit -> Clear (make sure the clear fill color is set to white)

**3)** Use the rectangle selection tool + File -> Save as -> .tiff to save the leaf discs for each genotype as a single image (see sample data)
   
Note: Be very sure that the leaf discs are spaced properly and the discs are fully in the image, not touching the edge in any way!

Note: For higher volume experiments with more timepoints, I have written a Fiji macro that will auto crop and name images with from simple text file of genotype names and coords (available upon request)



## Main Pipeline
![RGB_Image_LeafDiscAssy_SampleDataSet_Final13](https://github.com/RichardTegtmeier/Fire-Blight-Leaf-Disc-Assay/assets/55664780/ed52c896-5087-45e3-800b-3af5402dcb34) ![Class_Image_LeafDiscAssy_SampleDataSet_Final13](https://github.com/RichardTegtmeier/Fire-Blight-Leaf-Disc-Assay/assets/55664780/b37c160d-81b6-4d6d-8e26-e48717d6c8c9) 

**1)** Download the .ipynb file, sample data and LeafDiscPDF_LowD.txt

**2)** Run the first chunk of code to import all libraries and functions (for installing I prefer !pip install [name] in JupyterNotebook)

**3)** Change the names of the final output data set (default is .csv to analyze in R) and specific paths to your files

**data_name_out (string):** The name of the final dataset output (without .csv in name)

**folder_path (string):** Full path to the folder containing images to analyze.

**output_folder_path (string):** WorkDir - The full path where the classified and cropped images output

**pdf_file_name (string):** The full path to the txt file with the probability density function (PDF)

**4)** Run the final function fb_detached_leaf_assay(folder_path, data_name_out, output_folder_path, pdf_file_name, 15,15)

**NOTE:** The 15 row x 15 column grid number is arbitrary, but useful. A 15x15 grid ensures each disc is separated and analyzed individually, if you have issues with 2 discs read as 1, try increasing these numbers) 






