## Server Connection

This section is for internal team use only. 

## Connect to Server

Use the following command to `ssh` into our server. 
```
ssh xuanyu@rackjesh.ucsd.edu
```
When prompted, enter our secret password. As the `conda` environment is properly
set up, we would see command line prompt:
```
(base) xuanyu@rackjesh:~$
```
We can now execute any `python` and `conda` commands remotely on the server. 

**Note**: The default (`base` environment) python version is `Python 3.7.4` and conda version is `Conda 4.7.12`. We can verify this by
```
python --version
conda info
```

## Anaconda Environments

Our work for Debatestar project uses its own conda environment named `debatestar`. 
We can activate and deactivate the environment using the following commands:
```
conda activate debatestar
conda deactivate
```
Once our environment is activated, we shall see the command line prompt as:
```
(debatestar) xuanyu@rackjesh:~$
```
**Note**: make sure we do all our work using the same `debatestar` environment. 
This environment uses latest version of python: `Python 3.8.1`. It's a clean environment
with no extra packages installed. We need to manually `conda install` required packages.

To create new environments, type
```
conda create --name whatever-name python=3
```

All environments available can be listed with:
```
conda env list
```

## Jupyter Notebook Remote Access

**On Local Computer**

Connect local computer to the server and map the corresponding port:
```
ssh -L 8000:localhost:9999 xuanyu@rackjesh.ucsd.edu
```
We will be connected to the server as usual.

**On Remote Server**

First, make sure we are in `debatestar` conda environment. If not, type:
```
conda activate debatestar
```

Then launch the jupyter notebook on port 9999:
```
jupyter notebook --no-browser --port=9999
```
We will see the jupyter notebook up-and-running on remote server. 

Now, we can luanch the farmiliar GUI jupyter notebook on our local brower, by typing:
```
localhost:8000
```
**Note** It might prompt you to type the token shown on server. 







