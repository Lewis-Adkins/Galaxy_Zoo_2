# Galaxy_Zoo_2

The goal of this project is to analayze up to roughly 300,000 photos of galaxies and classify them based on their shapes (Spiral, elliptical, and irregular).

Step 1:
Download the photos off of Kaggle "Galaxy_Zoo_2"
https://www.kaggle.com/datasets/jaimetrickz/galaxy-zoo-2-images

Step 2: 
Create a folder named galaxy_data and extract all files into folder

Step 3:
Head over to the Glaxaxy Zoo 2 homepage and download the Table 1 - Normal-depth sample with new debiasing method csv file under the Galaxy Zoo 2 Section
Upload file to the galaxy_data folder.

Step 4:
Before running the notebook make sure you adjust your paramters before running:

    Parameters:
    frac_data     = percentage of data you desire from the ~300,000 photos for your data set
    frac_valid    = percentage of data you desire to test your model on. I would keep it above .001 to make sure you have photos for each category
    photo_size    = size of photos. Default is (424,424). I would keep it above (300,300) to make sure you get as much detail as possible for your model
    degree_range  = a debias method to rotate each of your photos in your dataset for different angles. (Optional: only if you have a more powerful computer, if not set to 0)
    batch_size    = how many photos do you want your model to read at a time
    epochs        = number of iterations/training loops you want your model to review your photos. Keep around 50-100 at most
    pretrained    = keep set to False with this version of the Resnet Model. Does not work with 'True'
    learning_rate = How fast you want your model to learn
    momentum      = I would not touch

Step 5:
Run cudacheck.ipynb to tell whether or not if you have cuda installed on your machine. this is a large dataset and would be advantageous to use as much acceleration as you can to help train your model

Step 6:
Run galaxy_classifcation.ipynb. If there are any errors try restarting the the cells and run again. All photos will be seperated by class and then further sepearted into your fraction of data that you would like in there folders. When everything is fully run and trained you can upload any photo from the validaiton folder to your model to test it.

