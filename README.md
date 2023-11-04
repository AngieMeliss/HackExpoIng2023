## HackExpoIng2023 - DataScience Project

# Land Mines

Detection of mines buried in the ground is very important in terms of safety of life and property. Many different methods have been used in this regard; however, it has not yet been possible to achieve 100% success. Mine detection process consists of sensor design, data analysis and decision algorithm phases. The magnetic anomaly method works according to the principle of measuring the anomalies resulting from the object in the magnetic field that disturbs the structure of it, the magnetic field, and the data obtained at this point are used to determine the conditions such as motion and position. The determination of parameters such as position, depth or direction of motion using magnetic anomaly has been carried out since 1970.

To replicate the results of this project, you can clone it directly in your colab notebook or in your local framework.

> To run it, you will need the dataSet, which you can download from https://archive.ics.uci.edu/dataset/763/land%2Bmines-1

> To obtain more context of the data, how it was obtained and its characteristics: http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8443331


*   **Preprocessing**

  The dataSet consists of 4 parameters: 
  - **V** Voltage: Output voltage value of FLC sensor due to magnetic distorsion.
  - **H** Height: The height of the sensor from the ground.
  - **S** Soil type: 6 different soil types depending on the moisture condition.
  - **M** Mine type: 5 different mine classes, which are commonly encountered on land.

  
  The mine types are as follows, and are labeled in the dataset like this: 
  
  1. 'Null'
  2. 'Anti-Tank'
  3. 'Anti-Personel'
  4. 'Booby-Trapped Anti-Personel'
  5. 'M14 Anti-Personel'

 Where Null means there is no mine
  
  The counting of the data by type of mine showed that each class has an average of 67 data, for a total of 338, which indicates that the data are well balanced, that is, they are not disproportionate and the study is not blinded.

  The data were explored using Seaborn's pairplot function to find how the variables relate to each other and it was found that the trends are very well defined, since the correlation is high between variables.
  
  Subsequently, a 3-dimensional PCA was performed and the relationship of the components was plotted again with a pairplot. With this, the hypothesis that there is a dominant variable was confirmed, since the variance of this component is 0.88, which indicates that it strongly represents the behavior of the data.
  You can find more detailed information in the Notebook `Preprocesamiento_Analisis.ipynb`


*   **Modelo**
