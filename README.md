# High-Resolution Analysis of Protoplanetary Disks with ALMA

This project utilizes high-resolution images of protoplanetary disks captured by ALMA, specifically from the DSHARP project data, to characterize the structures present in planet-forming disks.

## Analysis Steps:

1. **Image Loading and Visualization**:  
   Downloads continuum images (1.3 mm) centered on the target disk, such as the IM Lup disk. The images are plotted with overlaid major and minor axes based on parameters from Huang et al. (2018).

2. **Rotation and Deprojection**:  
   The image is rotated using the rotation matrix R(PA) to align with the position angle (PA), and deprojected in the plane of the sky, pixel by pixel, to achieve a face-on view of the disk.

3. **Conversion to Polar Coordinates**:  
   The image is transformed into polar coordinates to visualize the rings and spirals in terms of radius and azimuthal angle.

4. **Radial Profile Plotting**:  
   Calculates and plots the radial profile by averaging flux density at each radial point and computing the standard deviation, effectively collapsing the 2D data along the azimuthal axis.

5. **Azimuthally Averaged Image and Unsharp Masking**:  
   Creates an azimuthally averaged 2D image using the radial profile to produce a smooth ring pattern, then subtracts it from the deprojected image to highlight non-azimuthal features using unsharp masking.

6. **Bonus - Residuals in Sky Coordinates**:  
   Transforms the azimuthally averaged image back to sky coordinates and subtracts it from the original image to display residuals in equatorial coordinates.

## Requirements:
- Python 3.x
- `astropy`
- `scipy`
- `matplotlib`
- `numpy`

## Usage:
Clone or download the repository, and run the Jupyter notebook provided to analyze the protoplanetary disk images step by step. For any questions or inquiries feel Free to contact me by email (nicolas.campos.a@usach.cl), or my dear friend Vicente who also work on the code development (vicente.silva.g@usach.cl)
