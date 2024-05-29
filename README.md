# no-show-analysis

This is an analysis of no-show medical appointments in Brazil.
This data set originates from https://www.kaggle.com/datasets/joniarroba/noshowappointments.

Medical facilities around the world have a common problem: patients who miss their appointments without prior notice to the facility. This is commonly referred to as a “no-show”.
These facilities need to have a method to predict and mitigate the impact of these no-show appointments, and this project builds a machine-learning model that can predict no-shows and identifies the top features that were be used to make this prediction.

This project is contained in a Jupyter Notebook with Python kernel and many useful libraries have been imported.  I engineered several features in this project.  

When I began this project, my target F-Score was 0.75 to consider the project a success. 

The supervised machine learning classification model achieved an F-score of 0.80, which exceeded the target score.  F-score was chosen as the target metric because this data set has a class imbalance, with about 20.2% in the no-show class and 79.8 % in the show class.  In the setting of imbalanced classes, calculating the precision and recall will reflect the impact of false positives and false negatives,  and the F-score is the harmonic mean of these metrics.   Out of all actual no-shows, this model can correctly predict them about 85% of the time, and of all patients predicted to no show, it was correct 76% of the time.  

The top 3 feature importances extracted from the model in rank order were:  
1. Previous patient no-shows.  This is by far the most predictive feature in prediction of a no-show with a normalized weight of 0.94!
2. Patient age was the second ranked feature with a normalized weight of 0.021
3. The date interval, or wait time between the date the appointment is made and the date of the actual appointment, was third with a normalized weight of 0.017.  

To view a rendering of this Jupyter Notebook from nbviewer that allows function of the embedded links,  please visit the link below. 

[nbviewer](https://nbviewer.org/github/LZNeill/no-show-analysis/blob/5ca9df3063eac0b94772ff1bc7ba036432dd3d0a/No%20Show%20Appointment%20Jupyter%20Notebook.ipynb#top)
