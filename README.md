# Sleepness Detection using Brain Waves
Introduction, overview, brief discussion about my project, and etc. 

# Prerequisites
-Python 3.x
-TensorFlow 1.8.0 (to check, run python -c "import tensorflow as tf; print(tf.__version__)")
-[SciPy](https://www.scipy.org/install.html)

### Setup
- Clone this repo: 
```bash
git clone https://github.com/elliottwu/sText2Image.git
cd sText2Image
```

- Download preprocessed CelebA data (~3GB): 
```bash
sh ./datasets/download_dataset.sh
```

### Train
```bash
sh train.sh
```
- To monitor training using Tensorboard, copy the following to your terminal and open `localhost:8888` in your browser
```bash
tensorboard --logdir=logs_face --port=8888
```

### Test
```bash
sh test.sh
```

### Pretrained Model
- Download pretrained model: 
```bash
sh download_pretrained_model.sh
```

- Test pretrained model on CelebA dataset: 
```bash
python test.py ./datasets/celeba/test/* --checkpointDir checkpoints_face_pretrained --maskType right --batchSize 64 --lam1 100 --lam2 1 --lam3 0.1 --lr 0.001 --nIter 1000 --outDir results_face_pretrained --text_vector_dim 18 --text_path datasets/celeba/imAttrs.pkl
```

# Acknowledgment
Part of the project was developed in Asian University Machine Learning Camp Jeju 2018. More interesting projects can be found in project descriptions and UMLC GitHub.

