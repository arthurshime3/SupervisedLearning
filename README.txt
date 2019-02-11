Project 1: Supervised Learning

Github: https://github.com/arthurshime3/SupervisedLearning

The datasets can be found at the following sources:
Titanic: https://www.kaggle.com/dmilla/introduction-to-decision-trees-titanic-dataset?fbclid=IwAR2wDL2sOlU1vRf4QY8h-FmWbXe0fb_S_dKrLDzzPrGeOJVjg4LvANazzLc
Adult: http://archive.ics.uci.edu/ml/datasets/Adult?fbclid=IwAR0lRjGu57NmSSrwT2F4UqH-9hyvtJrq9yGdzoUo8QsawnKgo7660AqD5Uw

The preprocessed data is already included in this repository so those can be downloaded and used instead of going to the original websites and downloading the datasets. 

All of the data for training, testing, and cross validation accuracy are stored in these sheets. The graphs used to display the data are also included:
Titanic: https://docs.google.com/spreadsheets/d/1-MNQovc6mK1Yt4EkBQP6MohO7cx-cQDj1LYs41Sb-pg/edit#gid=1920313251
Adult: https://docs.google.com/spreadsheets/d/15WZhfrUXd4xYVRBqwS8NkSmnuL9e3wVeenjXUMdAqF0/edit#gid=1499383213

To run the data:
If you are using the preprocessed data, skip to step 5. If you are working with unprocessed, original data taken from the links above, start here:
1. Download the data and import them into excel. The Titanic data can be processed using process.py which is included in the Titanic folder (a portion of this code was taken from the kaggle website where the dataset is from). This script will mark some of the values into groups and discretize them. Attributes and discretization of the Adult dataset was done by hand, where I found similar attribute values and grouped them together (the original and post processed files are included as examples but most of it was done by hand in excel). For the Adult dataset, I categorized grades below 4th as preschool, grades 4-11 as pre high school, college and associate school as college, and master, PHD, prof school,  etc into higher education. Marriage status was converted so that separated, widowed, divorced, are grouped together, as well as Native regions became continental regions. For Titanic, title, siblings, and parents were deleted and the python script discretized age and ticket price.

2. Open both files in Weka's explore section and apply the filter for randomize. Save them as arff files called randomTit.arff and adultRandomized.arff. 

3. Using another python script provided, divide the csv file into 10%, 20%, ..., 80% and save them. Save the last 20% of the data as the test set.

4. Convert each file into an arff file by importing them into Weka and saving them as arffs.

5. Using the randomized 80% file for each data, open them in Weka and run cross validation 10 fold using classifiers and tuned hyperparameters. The values of the hyperparameters can be found in the analysis.

6. Run the various classifiers using training, testing, and k-fold cross validation through the different training sizes (10%, 20%, ..., 80%). 
