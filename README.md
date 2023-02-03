# whisper-small-kr-fine-tune
Fine tune OpenAI whisper model on a korean dataset
This model is a fine-tuned version of [openai/whisper-small](https://huggingface.co/openai/whisper-small) on the Bingsu korean dataset. It achieves the following results:

### Training results
| Step | Training Loss | Validation Loss | Wer       |
|------|---------------|-----------------|-----------|
| 1000 | 0.1141        | 0.145484        | 10.811625 |
| 2000 | 0.0369        | 0.106371        | 7.72474   |
| 3000 | 0.0153        | 0.095729        | 6.520102  |

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 1e-05
- train_batch_size: 16
- eval_batch_size: 8
- seed: 42
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- lr_scheduler_warmup_steps: 500
- training_steps: 3000
- mixed_precision_training: Native AMP
