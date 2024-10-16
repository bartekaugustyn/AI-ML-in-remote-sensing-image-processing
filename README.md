# GZM Land Cover Classification Application

## **Usage Instruction**

To successfully utilize the GZM Land Cover Classification Application, please follow these steps:

- **Step 1**: Import GZM Boundaries
Import the Górnośląsko-Zagłębiowska Metropolis (GZM) boundaries into the Google Earth Engine (GEE) assets. Ensure that the boundaries are correctly set up for subsequent analyses.
![image](https://github.com/user-attachments/assets/aa3c4273-c5d9-42a2-ab06-ee7b96202550)


- **Step 2**: Import and Convert Reference Data
Import your reference data into GEE. If your reference data is in .txt format, copy the files and convert them using the provided conversion function. This step is crucial for preparing training data for the machine learning model.

![image](https://github.com/user-attachments/assets/83e7883c-6083-4ce9-b6df-ed1d1e7ebea9)

- **Step 3**: Import and Run the Code
Copy the provided code into the GEE Code Editor and execute it. This will initiate the process of land cover classification based on the input data.

## Application Overview
The GZM Land Cover Classification Application leverages Google Earth Engine (GEE) to classify land cover types within the Górnośląsko-Zagłębiowska Metropolis (GZM) region using machine learning techniques. The application employs a Random Forest classifier, which is a supervised learning algorithm renowned for its efficacy in classification tasks.

## Functionality Breakdown
Image Acquisition: The application begins by acquiring Landsat 9 Top of Atmosphere (TOA) imagery for the GZM area, filtered by a specified time frame (May to October 2023) and cloud cover. The images are processed to compute a median composite, which effectively reduces noise and improves the quality of the data.

## Pan Sharpening
 To enhance spatial resolution and visual clarity, the application applies a pan sharpening technique. This involves utilizing the HSV (Hue, Saturation, Value) color space to combine the RGB bands of the Landsat imagery with the near-infrared (NIR) band. The sharpened image is then displayed, significantly improving the visual representation of the land cover classes.
![image](https://github.com/user-attachments/assets/9ce83695-ff71-4494-89f3-2e31c27dd55a)
![image](https://github.com/user-attachments/assets/378d146a-aaa2-486d-a828-fef5a539b967)


### Training Data Preparation
The application utilizes manually labeled polygons representing different land cover types, including agriculture, urban areas, forests, and water bodies. This training data is crucial for teaching the classifier to differentiate between the various classes.

### Machine Learning Classification
The Random Forest classifier is trained using the spectral bands of the Landsat imagery sampled from the training data. This algorithm builds multiple decision trees and merges their outputs for more accurate classification results. Once trained, the classifier is applied to the entire Landsat image, generating a classified output that visualizes the distribution of land cover types across the GZM region.
![image](https://github.com/user-attachments/assets/f589d992-b1a3-43a0-8d56-433b6f09fa10)


### Area Calculation
 The application calculates the area covered by each land cover class, providing valuable insights into the spatial distribution of different types of land use within the GZM region. The calculated areas are displayed in the console for further analysis.

![image](https://github.com/user-attachments/assets/96145465-c02b-4e2d-b1c3-fb613dc7dc22)


### Index Calculations
 The application computes two significant indices: the Normalized Difference Vegetation Index (NDVI) and the Normalized Difference Water Index (NDWI). These indices are essential for assessing vegetation health and water content, respectively. Both indices are calculated over the entire GZM area and for each specific class, facilitating a detailed understanding of the environmental conditions.

- NDVI
![image](https://github.com/user-attachments/assets/ab056295-6942-496a-901c-6cf896588b6e)
![image](https://github.com/user-attachments/assets/de3b4370-5ef0-448b-89b1-49e4dd8956ba)


- NDWI
![image](https://github.com/user-attachments/assets/a61ae5ad-70ff-421f-b1fb-e530e01863cf)
![image](https://github.com/user-attachments/assets/3bfd0217-2a46-43c9-82d5-4ce61e7f7761)



## Conclusion
The GZM Land Cover Classification Application provides a robust framework for analyzing land cover changes within the Górnośląsko-Zagłębiowska Metropolis. By integrating advanced machine learning techniques with remote sensing data, the application not only enhances our understanding of land use dynamics but also serves as a vital tool for urban planning and environmental management.
