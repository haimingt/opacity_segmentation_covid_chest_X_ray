# opacity_segmentation_covid_chest_X_ray

This respository mains serves for the supplemental materials of the paper "Deep learning segmentation model for automated detection of the opacity regions in the chest X-rays of the Covid-19 positive patients and the application for disease severity".

The model_info directory contains 
- model_summary_and_training_metrics.txt -> the schema of the segmentation model used in this study, and the metrics of the training epochs
- resnet18_Unet_segmentation_model_weights.h5 -> the trained model weights for the above model, with resnet18 backbone and Unet schema 

The covid_rural_annot directory contains the raw images from the TCIA COVID-19 Datasets:
Desai, S., Baghal, A., Wongsurawat, T., Al-Shukri, S., Gates, K., Farmer, P., Rutherford, M., Blake, G.D., Nolan, T., Powell, T., Sexton, K., Bennett, W., Prior, F. (2020). Data from Chest Imaging with Clinical and Genomic Correlates Representing a Rural COVID-19 Positive Population [Data set]. The Cancer Imaging Archive. DOI: https://doi.org/10.7937/tcia.2020.py71-5978.

- jpgs -> COVID-19-X_ray_mode-patient_id_image_date-XR.jpg -> the raw X-ray image for the specific patient on a specific date
      -> COVID-19-X_ray_mode-patient_id_image_date-XR.json -> the segmentations for the left/right lungs as well as opacity regions
- pngs_masks -> COVID-19-X_ray_mode-patient_id_image_date-XR.png -> the masks corresponding to the raw X-ray images. The background has value 0, the opacity region has value 1.
- manual_segmentations_model_predictions -> COVID-19-X_ray_mode-patient_id_image_date-XR.jpg.png -> the predicted opacities 
- covid_rural_patient_info.csv -> the patient info, including height, weight, BMI, zipcode, infection status, ICU admission, mortality etc
- covid_rural_radiologist_notes.csv -> the radiologist notes for the raw images

#please note that, all the segmentations were manually labeled by authors of this study.
 
The raw image, patient_info and the radiologist notes were downloaded from the TGCIA COVID-19 dataset as described above.

The covid-chestxray-dataset contains the randomly selected raw images from the https://github.com/ieee8023/covid-chestxray-dataset.

- selected_images -> raw images as well as segmentation of json format
- selected_images_masks -> masks for the opacity regions, with 0 for background and 1 for the opacity region
- model_predictions -> the predicted opacity region by our model 


 
      
      
