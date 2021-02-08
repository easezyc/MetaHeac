# Learn to Expand Audience via Meta Hybrid Experts and Critics
This is an implementation of our paper **Learn to Expand Audience via Meta Hybrid Experts and Critics**.

## Requirements

- Python 3.6
- Pytorch > 1.0
- Pandas
- Numpy

## File Structure

```
.
├── code
│   ├── main.py             # Entry function
│   ├── model.py            # Models
│   ├── metamodel.py        # Training Model from a meta-learning perspective
│   ├── readme.md
│   └── run.py              # Training and Evaluating 
│   └── utils.py            # Some auxiliary classes
└── data
    ├── process.py          # Preprocess the original data
    ├── processed_data      # The folder to contain the processed data
```

## Dataset

We utilized the Tencent Look-alike Dataset. 
To download the dataset, you can use the following link: [Tencent Look-alike Dataset](https://algo.qq.com/archive.html?). Then put the data in `./data`.

You can use the following command to preprocess the dataset. 
The final data will be under `./data/processed_data`.

```python
python process.py
```

## Run

Parameter Configuration:

- task_count: the number of tasks in a mini-batch, default for `5`
- num_expert: the number of experts, default for `8`
- num_output: the number of critics, default for `5`
- seed: random seed, default for `2020`
- gpu: the index of gpu you will use, default for `0`
- batchsize: default for `512`

You can run this model through:

```powershell
python main.py --task_count 5 --num_expert 8 --output 5 --batchsize 512
```
