<div align="center">    
 
# 3D-stuff    

<!-- ![CI testing](https://github.com/PyTorchLightning/deep-learning-project-template/workflows/CI%20testing/badge.svg?branch=master&event=push) -->
![CI testing](https://github.com/Viibrant/3d-stuff/actions/workflows/ci-testing.yml)

<!--  
Conference   
-->   
</div>
 
## Description   
Project for 3d digits pattern recognition  

## How to run   
First, install dependencies   
```bash
# clone project   
git clone https://github.com/Viibrant/3d-stuff.git

# install project   
cd 3d-stuff
pip install -e .   
pip install -r requirements.txt
 ```   
 Next, navigate to any file and run it.   
 ```bash
# module folder
cd project

# run module (example: mnist as your main contribution)   
python lit_classifier_main.py    
```

## Imports
This project is setup as a package which means you can now easily import any file into any other file like so:
```python
from project.datasets.mnist import mnist
from project.lit_classifier_main import LitClassifier
from pytorch_lightning import Trainer

# model
model = LitClassifier()

# data
train, val, test = mnist()

# train
trainer = Trainer()
trainer.fit(model, train, val)

# test using the best model!
trainer.test(test_dataloaders=test)
```

### Citation   
```
@article{YourName,
  title={Your Title},
  author={Your team},
  journal={Location},
  year={Year}
}
```   
