# Basic Multi-GPU cloud Training job:

##### Notes: 
This notebook can take up to 4 hours to work through (Just because of training time). You should have no problem getting to the training in less than an hour. But if you want to complete it it will take longer.
This being said this notebook as is only netted me around 89% on this competition. I decided to press forward and generate a tutorial on multi-GPU training since I did not see many full walkthroughs available for this yet.

If you wanted to optimize further feel free to play around with any portion of the process be aware it may make you spend more time in this instance.

The GPU set-up I describe in here runs about ~$5 per hour. But google gives you $300 of credits to play with so unless you've used them all this should be free.
Make sure to delete your notebook once your done.

### Prerequisites. 

Have a GCP account (Google Cloud Platform) 
* If you don't it can be created here https://cloud.google.com/
* As of making this they offer a 1-year $300 credit to use their services for free.
* You may need to go into your IAM & Admin's Quota page(This can be found by searching IAM or quota in the search bar) and request to increase the for whatever GPU and region you are using. Google typically increases mine within 30 seconds of requesting.

Have a Kaggle Account
* https://www.kaggle.com/
* Download this zip file https://www.kaggle.com/c/plant-pathology-2020-fgvc7/data
* It can be downloaded from the download all button on this page. You may need to register for the contest in order to do so. There are no obligations to compete.

### Steps:

The set up I used from Google Cloud was us-east1-b N1: 8x vCPUs with 4 P100 GPU's

When you launch the AI Notebook: https://cloud.google.com/ai-platform-notebooks <- This link should work if you've created an account already.

Select Create New Notebook and use TensorFlow 2.1 then select Customize.

From there you will select the Region, Compute Instance and GPU count. I used P100s because that was what was available in the region I chose and it did the job. 
But, any 4 GPU setup should be compatible with this tutorial. 

After it spins up it will display a button that says Open Jupyter Notebooks. Click on this.

Once inside the notebooks create a new terminal and clone this repository using the command below:

git clone https://github.com/Zethtren/Plants_Kaggle.git

Above the file manager in the notebook there will an option to upload files. Upload the Kaggle Data you downloaded earlier.

Once the file completes you should be able to run the notebooks in this order -> DataFrame_Build -> Model_DataGen

After running the two notebooks you will have a kaggle submission ready for the competition you registered for earlier.

If you want to use this submission I recommend downloading it to submit since doing this from GCP is complicated. SImply right-click the file that was created and click download.



