# QA_app_new

This is a quality assessment app developed initially for visualizing and manually assessing the quality of physiological data for the NKI Rockland dataset. It requires first plotting out the physiological signals in a visually assessiable form and organizing png files corresponding to each subject. Then, the user can launch the app and use the sorting buttons and comment box to generate a single csv result file that includes the classification results for each subject(i.e. plot). The details on how to set up the app is listed below. 

## How to use
#### 1. Downloading
Clone or download this repository on to your machine. 

#### 2. Organize your files
Take all the `png` files of plots of the physiological signals and put them into the `Plots` folder. This app is currently specifically designed for the preprocessed NKI Rockland dataset, and therefore, the naming convention of the file must follow a certain format(e.g. `sub-A00038189_ses-BAS1_task-rest_acq-1400_physio.png`). To use this app for other datasets, you will need to make adjustments to portions of code in the app. 

#### 3. (Importamt) Set up filepath
Launch MATLAB and type `appdesigner` in the console. Once the app designer launches, open this app. Click on "Code View"

![WechatIMG365](https://github.com/rachel0427/QA_app_new/assets/55034774/3773bb1f-69e2-43b3-a115-453f24b996e7)

Navigate to the `properties` function and locate the line of code that defines the property `myPath`. Change this to the location of this repository on your own machine.

![image](https://github.com/rachel0427/QA_app_new/assets/55034774/b9596f75-333f-4f94-b023-b6ea175600e8)

#### 4. Launch the app
After you save your changes, you are ready to begin using this app. You can either launch it by clicking the `QA_App_New.mlapp` file downloaded from this repository or clicking the "Play" button in MATLAB. After the app is launched, you should see this interface with the image in the middle being the first plot in your `Plots` folder. 

![image](https://github.com/rachel0427/QA_app_new/assets/55034774/7b42ad1a-ce9e-442c-b4d3-db040b9937f1)

The first row of buttons allows you to classify a general quality of the signal combining your assessment for both the cardiac and respiration signal. Then you can go into more detail and provide classifications for the cardiac signal and respiration signal separately by clicking the buttons on corresponding rows. For each plot you are sorting, you can type in some comment in the text box at the bottom and click the `Add comment` to add a line of comment for future reference. 

#### 5. Checking the result
The output of this app is a csv file that will be created when the app is launched for the first time. The file will be automatically generated in the repository directory and named `result.csv`. 

#### Note: 
progress will be saved in the result.csv file, so you can close the app at anytime and continue at a later time as long as you do not make any changes to the repository structure or the output file name. 
