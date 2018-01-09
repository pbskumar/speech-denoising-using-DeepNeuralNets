# speech-denoising-using-DeepNeuralNets

In this project, Deep Neural Networks are used to build speech denoising models.
The models are trained on TIMIT dataset.

Please refer to report for detailed explanation of the project.


To execute the code follow these steps:

1. The project requires numpy, pandas, tensorflow (gpu/cpu), Keras, pickle to execute
2. Place TIMIT dataset in main-code folder for the speech_preprocessing.py to execute
3. Adjust any necessary parameters (like path files) and run the 'speech_preprocessing.py'
4. Step 3 will create preprocessed data which will create test and train data of size 1.1GB
	When each noise and dB scale use 10 speeches
5. Next proceed to model.py file. Adjust flag in "if __main__" branch to run test or train parts
6. The functions are documented properly and are self explanatory.
7. train() creates models and saves to trained-models folder
8. test() function reads the save models and performs test on the test data.
9. After testing, the wave files generated are stored to "wavefiles" folder.
10. Then, execute stoi_test.m file adjusting necessary parameters to obtain stoi scores.
11. Little amount of post-processing is done in evaluate.py, which is optional. 
	It was written to facilitate the reporting process.


NOTE: Training took around 30-40 minutes on Google Compute Engine with 8 cores, and 2 Tesla K80 GPUs