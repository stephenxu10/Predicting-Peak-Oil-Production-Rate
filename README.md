# Project Title: Oil Production Predictor
Uses a Random Forest Regressor to calculate the peak rate of production for a given oil well, as described by the data features listed in cleaned_data.csv in this repo.

# Project Description

Our application is pre-trained on over 2,000 data points (distinct, existing wells run by Chevron). It takes in a CSV file containing the same features as training.csv (except for OilPeakRate). Not all features have to be filled in the input CSV, however, the features that are in cleaned_data.csv must all be filled in order for the model to run properly.

For your benefit, I have listed the required features here:
1. gross_perforated_length
2. number_of_stages	
3. total_proppant
4. total_fluid
5. true_vertical_depth
6. proppant_intensity
7. frac_fluid_intensity
8. average_stage_length
9. frac_fluid_to_proppant_ratio
10. bin_lateral_length
11. batch_frac_classification
12. well_family_relationship

## Technologies used

In this project, we used Python packages that are common in data analysis and AI: some notable ones include seaborn, numpy, pandas, and sklearn. We used Python for its wide access to powerful tools and libraries, and for its quick and easy scripting nature. This project does not require particularly fast or powerful computing measures, sophisticated communication over networks, or a well-designed front-end. As a result, these factors make Python the ideal language for us to write in.

## Challenges Encountered

Some challenges we faced in creating this project include understanding the physical meaning behind the different features of the provided training data. After speaking to the Chevron-track mentor (huge thanks for Timothy's patience and helpfulness), our team was much more prepared to clean and analyze the data. Additionally, we struggled with identifying the best data model to use -- we experimented with 2 and 3-layer neural networks using the Keras APIs from the TensorFlow package, the Elastic Net Model (a method that regularizes regression models), and the LightGBM API (a gradient-boosting framework utilizing tree-based algorithms). In the end, we settled on the Random Forest Regressor for its low RMSE and high r^2 value.

## Future improvements

In the future, we look to acquire more data to train the model further and make it more accurate. Additionally, we aim to incorporate position-based data into our model successfully. We didn't think the position data had correlation with the peak production rate as the data being deliberately anonymized for privacy reasons. Going forward, with more time and resources, we would like to develop compatability with various positional datapoints, including well and toe coordinates.

# Setting Up Your Environment

1. In your terminal, ```cd``` into the directory that you want the app to be in.
2. Type in ```git clone https://github.com/stephenxu10/Rice-Datathon-2024``` -- make sure that you clone the main branch!
3. Make sure you have Python installed on your computer. Python 3 is recommended, but Python 2 should work (has not been tested yet).
4. ```pip install``` any packages that you are missing. The packages are numpy, pandas, seaborn, matplotlib, warnings, and typing. This app does not require a specific version of any of these packages to run -- the latest verion should be sufficient.

# How to Run the Project
1. Put your properly formatted CSV (according to above specifications) in the same directory as model_building.ipynb.
2. Click the "Run all" button.
3. The results will appear in a new .xlsx file under the Submissions directory, and are also visible in the Juypter Notebook itself.

# Credits
Developers:
David Zhu
Liam Ruiz
Jason Han
Stephen Xu

Big thanks to Chevron for sponsoring this track, MLH for hosting this event, and the mentors for their valuable time and advice.