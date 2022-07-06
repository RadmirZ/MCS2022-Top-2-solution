# MCS2022.CarVerification 

Top 2 solution. Team "MiniFlex" RostislavK | RadmirZ

Competition: https://ods.ai/competitions/mcs_car_verification

| # |   ROC AUC   |   Domain 1   |   Domain 2   |   Domain 3   |   Domain 4   |   Domain 5   |
|---|:-----------:|-------------:|-------------:|-------------:|-------------:|-------------:|
| 1 |    0.97571  |     0.985    |    0.944     |    0.992     |    0.982     |    0.994     |

# Train and eval

## Preparation
1. Prepare datasets folder
```
├── datasets
│   ├── public_test
│   └── vehicle_models
└── MCS2022.CarVerification
    ├── <all_sources>
    ├── checkpoints
    ├── database
    └── logs
```

2. Install requirements.txt (tested for python3.6):
```bash
pip install -r requirements.txt
```

## Train
```bash
cd MCS2022.CarVerification
python train.py
```

## Generate database
Change *PRETRAIN* variable inside generate_database.py
```bash
cd MCS2022.CarVerification
python generate_database.py
```

## Inference
Use *scripts/ckpt_to_model.py* to convert checkpoints to model weights.

Change filenames inside *make_submit.py*

```bash
cd MCS2022.CarVerification
python make_submit.py
```

# References
- https://github.com/layumi/Person_reID_baseline_pytorch
- https://github.com/KevinMusgrave/pytorch-metric-learning
- https://github.com/abhuse/pytorch-efficientnet
