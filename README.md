# PLM-VF  
Introduction
# Package requirement  
  pytorch==2.1.2  
  scikit-learn==1.5.1  
  pandas==2.2.2  
# Test on the model  
## Preparing the input data  
First, you need to generate the input for the test dataset samples using the ProtT5 and ESM1b models. The input should be a tensor of dimension 2305, where:  
* The first dimension represents the sample labels.
* Dimensions 2 to 1025 are the ProtT5 embeddings of the sample.
* Dimensions 1026 to 2305 are the ESM-1b embeddings of the sample.

The processed test dataset `test_data.pt` can be found here: (Google Drive URL).  
## Usage
Once your inputs are prepared, you can proceed to testing using the provided `test.py` script.

The `test.py` script is designed to accept command-line arguments for the model file, test data, and output path. To run the script, you must specify each of these parameters using the appropriate flags. Below is a general format for running the script:
```
python test.py -m [path_to_model] -i [path_to_test_data] -o [path_to_output_csv_file]
```
