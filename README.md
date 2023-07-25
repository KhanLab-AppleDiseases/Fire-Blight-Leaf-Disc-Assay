# Fire Blight Leaf Disc Assay
The image analysis pipeline from the paper "An image-analysis based leaf disc assay for the rapid evaluation of genetic resistance to fire blight in apple".

## Basic Usage
Language: Python

This code was written using JupyterNotebook, so it is suggested to continue using IDEs compatible with the .ipynb filetype (i.e. JupyterNotebook, VSCode, etc.)

## Preprocessing
Software: ImageJ (Fiji) 

![image](https://github.com/RichardTegtmeier/Fire-Blight-Leaf-Disc-Assay/assets/55664780/d0ecad09-d52a-4b38-8117-fc6625ad4f90)

1) Use the image -> transform options to properly orient the full tray image
2) Use the polygon selections + Edit -> Clear (make sure the clear fill color is set to white)
3) Use the rectangle selection tool + File -> Save as -> .tiff to save the leaf discs for each genotype as a single image (see sample data)
   
Note: Be very sure that the leaf discs are spaced properly and the discs are fully in the image, not touching the edge in any way!

Note: For higher volume experiments with more timepoints, I have written a Fiji macro that will auto crop and name images with from simple text file of genotype names and coords (available upon request)



## Main Pipeline
![RGB_Image_LeafDiscAssy_SampleDataSet_Final13](https://github.com/RichardTegtmeier/Fire-Blight-Leaf-Disc-Assay/assets/55664780/ed52c896-5087-45e3-800b-3af5402dcb34) ![Class_Image_LeafDiscAssy_SampleDataSet_Final13](https://github.com/RichardTegtmeier/Fire-Blight-Leaf-Disc-Assay/assets/55664780/b37c160d-81b6-4d6d-8e26-e48717d6c8c9) 

1) Download the .ipynb file, sample data and LeafDiscPDF_LowD.txt
2) 

#Input all output and file names here

folder_path (string): Full path to the folder containing images to analyze.
data_name_out (string): The name of the final dataset output (without .csv in name)
#output_folder_path (string): WorkDir - The full path where the classified and cropped images output
#pdf_file_name (string): The full path to the txt file with the probability density function (PDF)

#nrow (int): number of rows plantcv will use to make grid  (more is better otherwise, two disks can get grouped)

#ncol (int): number of cols plantcv will use to make grid (more is better otherwise, two disks can get grouped)
    
data_name_out = 'LeafDiscAssy_SampleDataSet_Final'
folder_path = "C:\\Users\\[[Your Full Path]]\\Sample_Data\\"
output_folder_path = 'C:\\Users\\[[Your User Name]]\\Downloads\\'
pdf_file_name = 'LeafDiscPDF_LowD.txt' #must be in output_folder_path (WorkDir)





