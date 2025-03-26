# **Crime Analysis Report**

## **1. Introduction**

This report investigates crime statistics within the Los Angeles (LA) area from 2020 to the present. The dataset, obtained from [Data.gov](https://www.data.gov/), includes records of over 103 different types of crimes. The central research question guiding this analysis is:

> **What is the most likely crime in each area of Downtown LA?**

### **1.1 Data Source**

- **Source:** [Data.gov](https://www.data.gov/)  
- **Dataset:** Crime statistics within the LA area from 2020 to present  
- **Number of crime types:** 103+  

## **2. Research Question**

The primary goal of this project is to determine the type of crime that is most likely to occur in each Downtown LA area. Specifically, we want to identify trends based on:

- **Target Variable:** Crime Description (i.e., the specific type of crime)  
- **Predictor Factors:**  
  1. **Area** – The area or neighborhood within Downtown LA  
  2. **Sex of Criminal** – Male or Female  
  3. **Time of Day** – Morning, Afternoon, Evening, or Night  

## **3. Data Cleaning and Preparation**

Several preprocessing steps were performed:

1. **Outlier Detection & Removal:**  
   - Removed rows with missing or incomplete data (e.g., missing sex, location, or time).  
   - Ensured only valid lat/long coordinates for LA areas.

2. **Feature Engineering:**  
   - Categorized the **Time of Day** into discrete bins (Morning, Afternoon, Evening, Night).  
   - Encoded the **Sex of Criminal** (Male, Female) for further analysis.  

3. **Data Splitting:**  
   - Data was split into a **training** set (80%) and a **test** set (20%).  

## **4. Training Process**

Multiple models were tested to predict the **Crime Description** from the given predictors (Area, Sex, Time of Day). The training process took approximately 6 minutes and covered different model scenarios. Key details:

- **Model Selection:** Various classification models were evaluated.  
- **Performance Metric:** The **R²** score was recorded to measure how well the model predicts crime type from the given predictors.  

> **Final Model R²:** 99.55%  

This high R² score indicates that the model is able to explain approximately 99.55% of the variance in crime type based on the area, sex of the criminal, and time of day.

## **5. Results**

1. **Most Likely Crime by Area**  
   - Each area within Downtown LA tends to have a particular crime that dominates.  
   - Common patterns emerged, showing certain areas had higher likelihoods of specific offenses (e.g., theft, assault, vandalism).

2. **Influence of Time of Day**  
   - Evening and Night-time spikes in certain crimes (e.g., assault, burglary).  
   - Morning hours associated with fewer, often property-related incidents.  

3. **Influence of Sex of Criminal**  
   - Some areas showed a higher proportion of arrests involving male perpetrators.  
   - Limited instances in specific crime categories involving female suspects.

## **6. Conclusion**

This analysis suggests that crime distribution varies by location, sex of the criminal, and time of day. With an **R² score of 99.55%**, the model is highly predictive. The insights can be leveraged by law enforcement agencies to allocate resources more effectively, focusing on specific hotspots and peak hours for each crime type.

## **7. References**

- [Data.gov](https://www.data.gov/) – LA Crime Datasets  
- LA Police Department Public Records  

