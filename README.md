# Chang Gung Fundus Database
Author: Jung-Sheng (Ryan) Chen

Updated on 03FEB2021.

## Overview
Chang Gung Fundus Database (CGFD) is a large thematic database comprising deidentified color fundus images associated with over twenty-five thousand patients who visited the ophthalmology department in the Linko branch, Chang Gung Memorial Hospital between January 2004, and October 2018. This thematic database includes information such as demographics, diagnosis records for each medical encounter during study period, laboratory test results, procedures, medications, and costs et al. The data structure was displayed in figure 1.
CG Fundus Database supports a diverse range of analytic studies spanning epidemiology, artificial intelligence, and electronic tool development. 
Researchers seeking to use the database must request access by providing a study proposal to the Center for Artificial Intelligence in Medicine, Chang Gung Memorial Hospital.

 
![Figure 1. The Data Structure of CG Fundus Database.](https://github.com/JSChen0404/Chang-Gung-Fundus-Database/blob/main/CG-Fundus-Database.png)

## Patient Definition
The study population included patients who visited the ophthalmology department and had the color fundoscopic examination between January 2004 and October 2018. All color fundus images during the study period were collected. Finally, the database comprises 384,743 color fundus images from 25,605 patients and 51,718 examinations.

## Electronic Health Record
CGFD included electronic health record (EHR) to store and process clinical data. A collection of images associated with a single report is referred to as a study. We queried the CGFD EHR for fundoscopic examination made in the Linko branch between January 2014 and October 2018 and extracted the set of patient identifiers associated with these studies. We subsequently extracted all diagnosis codes of outpatient visits and all laboratory data for this set of patients within the same period. The primary and secondary diagnosis codes was recorded using international statistical classification of diseases 9th version before 2015 and 10th revision after 2016. We retrieved the closest laboratory record for general laboratory items (e.g. WBC or HbA1c) within three months before and after examination date as their baseline laboratory values.
For anonymization purposes, we generated a random identifier for each patient with a prefix named “OPH” and a 6-digit numbers started from 000001 to 025605. We refer to the anonymized identifier as the Encrypted_ID. In addition, we generated a random identifier for each patient in the range 1-100. All date-format variables (such as birthdate, examination date, and others) were shift with adding this random identifier by each patient. This ensures anonymity of the data while preserving the relative chronology of patient information, which is crucial for appropriate processing of the data. We refer the shifted dates for birthdate and examination date as the Encrypted_Exam_Date and Encrypted_Birthday.

## Codebook
![Table 1. Codebook.](https://github.com/JSChen0404/Chang-Gung-Fundus-Database/blob/main/Codebook.jpg)

## Data Statistics
![Table 2. Data Statistics.](https://github.com/JSChen0404/Chang-Gung-Fundus-Database/blob/main/data%20stat.jpg)

## Color Fundoscopic Examination
Fundoscopic examination uses a magnifying lens and a light to check the fundus of the eye (back of the inside of the eye, including the retina and optic nerve). The ophthalmoscope illuminates the retina through the normal iris defect that is the pupil. Visualization of the retina can provide lots of information about a medical diagnosis. These diagnoses include high blood pressure, diabetes, increased pressure in the brain and infections like endocarditis. Around 3~15 fundus photos may be taken in one examination and one of them was a summary picture for corresponding exam. This database contains 384,743 photos from 51,718 examinations. For anonymization purposes, all patient information on the photos were de-identified. 

![Figure 2. Sample Fundus Photos.](https://github.com/JSChen0404/Chang-Gung-Fundus-Database/blob/main/sample%20data.jpg)

## Requesting Data access
To request a dataset, please contact the Center of Artificial Intelligence in Medicine at cgmhailab@gmail.com

## License agreement
This dataset is made freely available to academic and non-academic entities for non-commercial purposes such as academic research, teaching, scientific publications, or personal experimentation. Permission is granted to use the data given that you agree:

1. That the dataset comes “AS IS”, without express or implied warranty. Although every effort has been made to ensure accuracy, we (Center for Artificial Intelligence in Medicine from Chang Gung Memorial Hospital) do not accept any responsibility for errors or omissions.
2. That you include a reference to the Chang Gung Fundus Database in any work that makes use of the dataset. Cite the following sentence: Chang Gung Fundus Database from the Center for Artificial Intelligence in Medicine of Chang Gung Memorial Hospital.
3. That you do not distribute this dataset or modified versions. It is permissible to distribute derivative works in as far as they are abstract representations of this dataset (such as models trained on it or additional annotations that do not directly include any of our data) and do not allow to recover the dataset or something similar in character.
4. That you may not use the dataset or any derivative work for commercial purposes as, for example, licensing or selling the data, or using the data with a purpose to procure a commercial gain.
5. That all rights not expressly granted to you are reserved by us (Center for Artificial Intelligence in Medicine, Chang Gung Memorial Hospital).


