## Decentralized Policy Learning with Partial Observation and Mechanical Constraints

This is the python code for Decentralized Policy Learning with Partial Observation and Mechanical Constraints for Multi-person Modeling.

## Author
Keisuke Fujii - https://sites.google.com/site/keisuke1986en/

## Reference
Keisuke Fujii, Naoya Takeishi, Yoshinobu Kawahara,Kazuya Takeda, "Decentralized Policy Learning with Partial Observation and Mechanical Constraints for Multi-person Modeling", arXiv preprint arXiv:2007.03155, 2020
https://arxiv.org/abs/2007.03155

## Requirements

* python 3.6 
* To install requirements:

```setup
pip install -r requirements.txt
```

## Usage
 
* Run `run.sh` for a simiple demonstration of training and test using the NBA dataset (only one game).

* Actual commands in training and test of our model are also in `run.sh` (commented).  

* Data can be downloaded from https://github.com/rajshah4/BasketballData

## Note for using your own data

* There may be trade-offs between training data size and model (and movement) complexity.
* For example, if you have smaller data and the movement is simple, you can use simple model such as RNN. 

## Pretrained Models

You can download pretrained models from `weights/` for NBA dataset as discussed in the paper.

## Results

Our model achieves the following performance (Table 2 in the paper):

| Model name            |   position    |   velocity    |  acceleration  |
| ----------------------|-------------- | ------------- | -------------- |
| 1. Velocity           | 1.41 +/- 0.34 | 1.08 +/- 0.21 | 10.90 +/- 2.09 |  
| 2. RNN-Gauss          | 1.31 +/- 0.32 | 1.05 +/- 0.13 |  1.88 +/- 0.30 |
| 3. VRNN               | 0.71 +/- 0.17 | 0.68 +/- 0.10 |  1.43 +/- 0.20 |  
| 4. VRNN-macro         | 0.71 +/- 0.17 | 0.68 +/- 0.10 |  1.43 +/- 0.20 |
| 5. VRNN-Mech          | 0.69 +/- 0.17 | 0.68 +/- 0.10 |  1.37 +/- 0.20 |
| 6. VRNN-Bi            | 0.72 +/- 0.19 | 0.66 +/- 0.10 |  1.36 +/- 0.19 |
| 7. VRNN-macro-Bi-Mech | 0.73 +/- 0.18 | 0.68 +/- 0.10 |  1.34 +/- 0.19 |
