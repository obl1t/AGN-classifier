## AGN Classifier
This repository contains a crossmatched data file of approximately 4800 Active Galactic nuclei. Data was crossmatched from SDSS SpecObj and VeronCAT. \
This repository also contains a Python notebook containing a pipeline that trained a KNN and Dense Neural Network using the crossmatched data: 
- Pertinent values of each line of the crossmatched CSV are extracted, namely the Plate, MJD, FiberID, object type, and redshift.
- For each line, the Plate, MJD, and FiberID are used to reconstruct a SDSS science archive server url to download the spectra .fits file.
- The spectral data from the .fits files are downloaded and used to create a training file, containing the spectral information and redshift as features, and the object type as the target.
- A KNN is trained using a dataframe created from the training file. 50 KNN models are created with varying random states, and the accuracies are aggregated.
- A Dense Neural Network is also trained, with a 128-64-3 hidden layer pattern.

### TODO: improve readibility of .ipynb. Create a user-interface wrapper for the machine learning model. 

