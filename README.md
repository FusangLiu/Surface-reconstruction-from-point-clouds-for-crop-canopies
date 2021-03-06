# Surface-reconstruction-from-point-clouds-for-crop-canopies
The surface reconstruction is a Crust-based method which firstly adopts the Crust method to triangulation and then uses a statistic method to filter abnormal facets (i.e. triangles).The output plant model can be used to directly calculate the leaf area and link to ray-tracing models for canopy photosynthesis calculation.  

![alt text](https://github.com/FusangLiu/Suface-reconstruction-form-point-clouds-for-crop-canopies/blob/main/Fig5.jpg)
Fig. 1. An example of the UAV-derived canopy architecture model before (A) and after (B) removing abnormal facets. The canopy architecture model was generated from the vegetation point cloud of the inter-cropped maize/soybean canopy at 70 days after sowing. The purple colour indicates abnormal facets.


# Reference
Liu F, Hu P, Zheng B, Tao D, Zhu B, Guo Y. 2021. A field-based high-throughput method for acquiring canopy architecture using unmanned aerial vehicle images. Agricultural and Forest Meteorology 296, 108231. https://doi.org/10.1016/j.agrformet.2020.108231


# Software information
This software is based on MATLAB R2020b.Before you use the software, you should verify that version 9.9 (R2020b) of the MATLAB Runtime is installed.   
If not, you can download and install the Windows version of the MATLAB Runtime for R2020b 
from the following link on the MathWorks website:
https://www.mathworks.com/products/compiler/mcr/index.html


Input：input file path, point clouds name, output file path, output plant model name, threshold of mesh outlier (default 3), threshold of surface smoothing (default 0.5), display(default 1)

Output: meshed_plant_model 


Note: 
1) The input point cloud must be from the PLY or PCD file
2) The output plant model is the PLY file which includes the point locations and triangle index.


# Example
### Using the software in the windows DOS command line:

E:\PCSR\PCSR.exe "E:\PCSR" "example_maize_pc.ply" "E:\PCSR" "example_maize_pm.ply"

E:\PCSR\PCSR.exe "E:\PCSR" "example_maize_pc.ply" "E:\PCSR" "example_maize_pm.ply" 3 0.5 1

### Using the software in the MATLAB:

cmd=['E:\PCSR\PCSR.exe "E:\PCSR" "example_maize_pc.ply" "E:\PCSR" "example_maize_pm.ply"']; 
system(cmd)

cmd=['E:\PCSR\PCSR.exe "E:\PCSR" "example_maize_pc.ply" "E:\PCSR" "example_maize_pm.ply" 3 0.5 1'];
system(cmd)
