# Tracking the frequency of phytoplankton clonal lineages using multispectral image flow cytometry and neural networks
## Github page     Tracking-clonal-lineages-using-AI-

Code and data for the neural network on feature values of Imagestream MK II on phytoplankton is structured into two folders:
In-silico: for the first set of test where the frequencies to be predicted were created via R from mono-culutres &
In-vitro: for the second tests where the frequencies to be predicted were mixed from fixed cultures of different clonal lineages

Both folders contain Rmd scripts for creating the NN models and running it over the prepared frequencies in the corresponding folders.
All raw data of mono-cultures for configuring the NN moddels and frequency predictions are available as well.

To run the scripts, we recommend the following order:
In the in-silico folder:
First: "Recall rate of K-fold and increasing training data.Rmd" this uses the data from the "Data for training size" folder
Second: "Creating 6clone model and running a small test.Rmd" & "Creating the paired models.Rmd" which create the NN with the data from the "Model configuration" folder and save them in the according name
Third: "Frequency prediction of 6clone model.Rmd" & "Frequency prediction of paired models.Rmd" which use the NN models, saved from the previous scripts and run predictions on the in-silico prepared frequencies from the "Frequencies" folder

In the in-vitro folder:
First: "Setting up keras model_CR2_CR7.Rmd" & "Setting up keras model_CR1_CR6.Rmd" which use the data from the ""Data for model set-up" folder to create NN and save them in the according name
Second: "Running the keras models_CR2_CR7.Rmd" & "Running the keras models_CR1_CR6.Rmd" which read in the NN and predict the in-vitro prepared frequencies in the folders "Raw Data/CR2-CR7 frequencies" & "Raw Data/CR1-CR6 frequencies"
