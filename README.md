# LUT Model

## This will be the overall stucture of the LUT model and how it will operate. There will be a python script called Model_Parameters.py. In this script you will specify which model(Baseline,SCI) and other network parameters that we will vary as time goes on. Then the flow of the model will be the following

## Build network
```
python Build_network.py
```
## Compile mod files
```
cd biophys_components/mechaisms
nrnivmodl modfiles
cd ../..
```
## Run network
```
python run_network.py
```
## Check results
```
python plot_results.py
```
## The file structure of the whole model will be 
| python file |use      |
|----------- | ----------- |
| build_network.py     |build network files            |
| run_network.py       |run network            | 
| plot_results.py      |plot simulation results            |
| model_parameters.py  |adjust network parameters                |
| feedback_loop.py     |BMTK module for feedback                  |
| bladder_equations.py |biophysical bladder eqautions stored here                 |
| build_inputs.py      |build inputs for network                 |
| synapses.py          |Loads custom neuron synapses                 |
| biophys_components   |Stores cell templates and modfiles                 |
| network              |Stores network files                 |
