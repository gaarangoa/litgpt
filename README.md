# LitGPT

# Use, finetune, pretrain, and deploy LLMs Lightning fast
Every LLM is implemented from scratch with **no abstractions** and **full control**, making them blazing fast, minimal, and performant at enterprise scale.

# Quick start
Install LitGPT
```
pip install 'litgpt[all]'
```

Load and use any of the [20+ LLMs](#choose-from-20-llms):   
```python
from litgpt import LLM

llm = LLM.load("microsoft/phi-2")
text = llm.generate("Fix the spelling: Every fall, the familly goes to the mountains.")
print(text)
# Corrected Sentence: Every fall, the family goes to the mountains.       
```

<details>
  <summary>Advanced install options</summary>

Install from source:

```bash
git clone https://github.com/Lightning-AI/litgpt
cd litgpt
pip install -e '.[all]'
```
</details>

[Explore the full Python API docs](tutorials/python-api.md).

---
# Choose from 20+ LLMs
Every model is written from scratch to maximize performance and remove layers of abstraction:   

| Model | Model size | Author | Reference |
|----|----|----|----|
| Llama 3, 3.1, 3.2 | 1B, 3B, 8B, 70B, 405B | Meta AI | [Meta AI 2024](https://github.com/meta-llama/llama3)                                           |
| Code Llama | 7B, 13B, 34B, 70B | Meta AI | [Rozière et al. 2023](https://arxiv.org/abs/2308.12950)                                       |
| Mixtral MoE | 8x7B | Mistral AI | [Mistral AI 2023](https://mistral.ai/news/mixtral-of-experts/)                                         |
| Mistral | 7B, 123B | Mistral AI | [Mistral AI 2023](https://mistral.ai/news/announcing-mistral-7b/)                                      |
| CodeGemma | 7B | Google | [Google Team, Google Deepmind](https://ai.google.dev/gemma/docs/codegemma)                                     |
| Gemma 2 | 2B, 9B, 27B | Google | [Google Team, Google Deepmind](https://storage.googleapis.com/deepmind-media/gemma/gemma-2-report.pdf)  |
| Phi 3 & 3.5   | 3.8B | Microsoft | [Abdin et al. 2024](https://arxiv.org/abs/2404.14219)                                                 |
| ... | ... | ... | ...   |

<details>
  <summary>See full list of 20+ LLMs</summary>

&nbsp;

#### All models

| Model | Model size | Author | Reference |
|----|----|----|----|
| CodeGemma | 7B | Google | [Google Team, Google Deepmind](https://ai.google.dev/gemma/docs/codegemma)                                                                 |
| Code Llama | 7B, 13B, 34B, 70B | Meta AI | [Rozière et al. 2023](https://arxiv.org/abs/2308.12950)                                                                   |
| Danube2 | 1.8B | H2O.ai | [H2O.ai](https://h2o.ai/platform/danube-1-8b/)                                                                                             |
| Dolly | 3B, 7B, 12B | Databricks | [Conover et al. 2023](https://www.databricks.com/blog/2023/04/12/dolly-first-open-commercially-viable-instruction-tuned-llm)      |
| Falcon | 7B, 40B, 180B | TII UAE | [TII 2023](https://falconllm.tii.ae)                                                                                              |
| FreeWilly2 (Stable Beluga 2) | 70B | Stability AI | [Stability AI 2023](https://stability.ai/blog/stable-beluga-large-instruction-fine-tuned-models)                 |
| Function Calling Llama 2 | 7B | Trelis | [Trelis et al. 2023](https://huggingface.co/Trelis/Llama-2-7b-chat-hf-function-calling-v2)                                  |
| Gemma | 2B, 7B | Google | [Google Team, Google Deepmind](https://storage.googleapis.com/deepmind-media/gemma/gemma-report.pdf)                                       |
| Gemma 2 | 9B, 27B | Google | [Google Team, Google Deepmind](https://storage.googleapis.com/deepmind-media/gemma/gemma-2-report.pdf)                                  |
| Llama 2 | 7B, 13B, 70B | Meta AI | [Touvron et al. 2023](https://arxiv.org/abs/2307.09288)                                                                           |
| Llama 3.1 | 8B, 70B | Meta AI | [Meta AI 2024](https://github.com/meta-llama/llama3)                                                                                 |
| Llama 3.2 | 1B, 3B | Meta AI | [Meta AI 2024](https://ai.meta.com/blog/llama-3-2-connect-2024-vision-edge-mobile-devices/)                                           |
| LongChat | 7B, 13B | LMSYS | [LongChat Team 2023](https://lmsys.org/blog/2023-06-29-longchat/)                                                                       |
| Mathstral | 7B | Mistral AI | [Mistral AI 2024](https://mistral.ai/news/mathstral/)                                                                                  |
| MicroLlama | 300M | Ken Wang | [MicroLlama repo](https://github.com/keeeeenw/MicroLlama)                                                                             |
| Mixtral MoE | 8x7B | Mistral AI | [Mistral AI 2023](https://mistral.ai/news/mixtral-of-experts/)                                                                     |
| Mistral | 7B, 123B | Mistral AI | [Mistral AI 2023](https://mistral.ai/news/announcing-mistral-7b/)                                                                  |
| Nous-Hermes | 7B, 13B, 70B | NousResearch | [Org page](https://huggingface.co/NousResearch)                                                                          |
| OpenLLaMA | 3B, 7B, 13B | OpenLM Research | [Geng & Liu 2023](https://github.com/openlm-research/open_llama)                                                         |
| Phi 1.5 & 2 | 1.3B, 2.7B | Microsoft Research  | [Li et al. 2023](https://arxiv.org/abs/2309.05463)                                                                  |
| Phi 3 | 3.8B | Microsoft Research | [Abdin et al. 2024](https://arxiv.org/abs/2404.14219)                                                                            |
| Platypus | 7B, 13B, 70B |  Lee et al. | [Lee, Hunter, and Ruiz 2023](https://arxiv.org/abs/2308.07317)                                                               |
| Pythia | {14,31,70,160,410}M, {1,1.4,2.8,6.9,12}B | EleutherAI | [Biderman et al. 2023](https://arxiv.org/abs/2304.01373)                                            |
| RedPajama-INCITE | 3B, 7B | Together | [Together 2023](https://together.ai/blog/redpajama-models-v1)                                                                 |
| StableCode | 3B | Stability AI | [Stability AI 2023](https://stability.ai/blog/stablecode-llm-generative-ai-coding)                                                  |
| StableLM  | 3B, 7B | Stability AI | [Stability AI 2023](https://github.com/Stability-AI/StableLM)                                                                    |
| StableLM Zephyr | 3B | Stability AI | [Stability AI 2023](https://stability.ai/blog/stablecode-llm-generative-ai-coding)                                             |
| TinyLlama | 1.1B | Zhang et al. | [Zhang et al. 2023](https://github.com/jzhang38/TinyLlama)                                                                         |
| Vicuna | 7B, 13B, 33B | LMSYS | [Li et al. 2023](https://lmsys.org/blog/2023-03-30-vicuna/)                                                                          |

**Tip**: You can list all available models by running the `litgpt download list` command.


</details>

&nbsp;

---

# Workflows
## Use using python jupyter

```python

from litgpt.finetune.lora import setup
from litgpt.args import TrainArgs

data = Alpaca(
    file_name = '../data/my_custom_dataset.json'
)

setup(
    checkpoint_dir='../models/checkpoints/EleutherAI/pythia-14m/',
    out_dir = '../models/custom-model/',
    data = data,
    train = TrainArgs(save_interval=1000,
                    log_interval=1,
                    global_batch_size=16,
                    micro_batch_size=1,
                    lr_warmup_steps=100,
                    lr_warmup_fraction=None,
                    epochs=1,
                    max_tokens=None,
                    max_steps=None,
                    max_seq_length=512,
                    tie_embeddings=None,
                    max_norm=None,
                    min_lr=6e-05)
)

```



Use the command line interface to run advanced workflows such as pretraining or finetuning on your own data.   


## All workflows   
After installing LitGPT, select the model and workflow to run (finetune, pretrain, evaluate, deploy, etc...):

```bash
# ligpt [action] [model]
litgpt  serve     meta-llama/Llama-3.2-3B-Instruct
litgpt  finetune  meta-llama/Llama-3.2-3B-Instruct
litgpt  pretrain  meta-llama/Llama-3.2-3B-Instruct
litgpt  chat      meta-llama/Llama-3.2-3B-Instruct
litgpt  evaluate  meta-llama/Llama-3.2-3B-Instruct
```

&nbsp;

---- 

## Finetune an LLM
Finetuning is the process of taking a pretrained AI model and further training it on a smaller, specialized dataset tailored to a specific task or application.


&nbsp;

```bash
# 0) setup your dataset
curl -L https://huggingface.co/datasets/ksaw008/finance_alpaca/resolve/main/finance_alpaca.json -o my_custom_dataset.json

# 1) Finetune a model (auto downloads weights)
litgpt finetune microsoft/phi-2 \
  --data JSON \
  --data.json_path my_custom_dataset.json \
  --data.val_split_fraction 0.1 \
  --out_dir out/custom-model

# 2) Test the model
litgpt chat out/custom-model/final

# 3) Deploy the model
litgpt serve out/custom-model/final
```

[Read the full finetuning docs](tutorials/finetune.md)

&nbsp;

---- 

## Deploy an LLM
Deploy a pretrained or finetune LLM to use it in real-world applications. Deploy, automatically sets up a web server that can be accessed by a website or app.   

```bash
# deploy an out-of-the-box LLM
litgpt serve microsoft/phi-2

# deploy your own trained model
litgpt serve path/to/microsoft/phi-2/checkpoint
```

<details>
  <summary>Show code to query server:</summary>

&nbsp;

Test the server in a separate terminal and integrate the model API into your AI product:
```python
# 3) Use the server (in a separate Python session)
import requests, json
response = requests.post(
    "http://127.0.0.1:8000/predict",
    json={"prompt": "Fix typos in the following sentence: Exampel input"}
)
print(response.json()["output"])
```
</details>

[Read the full deploy docs](tutorials/deploy.md).

&nbsp;

----

## Evaluate an LLM
Evaluate an LLM to test its performance on various tasks to see how well it understands and generates text. Simply put, we can evaluate things like how well would it do in college-level chemistry, coding, etc... (MMLU, Truthful QA, etc...)

```bash
litgpt evaluate microsoft/phi-2 --tasks 'truthfulqa_mc2,mmlu'
```

[Read the full evaluation docs](tutorials/evaluation.md).

&nbsp;

---- 

##  Test an LLM
Test how well the model works via an interactive chat. Use the `chat` command to chat, extract embeddings, etc...

Here's an example showing how to use the Phi-2 LLM:
```bash
litgpt chat microsoft/phi-2

>> Prompt: What do Llamas eat?
```

<details>
  <summary>Full code:</summary>

&nbsp;

```bash
# 1) List all supported LLMs
litgpt download list

# 2) Use a model (auto downloads weights)
litgpt chat microsoft/phi-2

>> Prompt: What do Llamas eat?
```

The download of certain models requires an additional access token. You can read more about this in the [download](tutorials/download_model_weights.md#specific-models-and-access-tokens) documentation. 

</details>

[Read the full chat docs](tutorials/inference.md).

&nbsp;

----

## Pretrain an LLM
Pretraining is the process of teaching an AI model by exposing it to a large amount of data before it is fine-tuned for specific tasks.

<details>
  <summary>Show code:</summary>

&nbsp;

```bash
mkdir -p custom_texts
curl https://www.gutenberg.org/cache/epub/24440/pg24440.txt --output custom_texts/book1.txt
curl https://www.gutenberg.org/cache/epub/26393/pg26393.txt --output custom_texts/book2.txt

# 1) Download a tokenizer
litgpt download EleutherAI/pythia-160m \
  --tokenizer_only True

# 2) Pretrain the model
litgpt pretrain EleutherAI/pythia-160m \
  --tokenizer_dir EleutherAI/pythia-160m \
  --data TextFiles \
  --data.train_data_path "custom_texts/" \
  --train.max_tokens 10_000_000 \
  --out_dir out/custom-model

# 3) Test the model
litgpt chat out/custom-model/final
```
</details>

[Read the full pretraining docs](tutorials/pretrain.md)

&nbsp;

---- 

## Continue pretraining an LLM
Continued pretraining is another way of finetuning that specializes an already pretrained model by training on custom data:

<details>
  <summary>Show code:</summary>

&nbsp;

```bash
mkdir -p custom_texts
curl https://www.gutenberg.org/cache/epub/24440/pg24440.txt --output custom_texts/book1.txt
curl https://www.gutenberg.org/cache/epub/26393/pg26393.txt --output custom_texts/book2.txt

# 1) Continue pretraining a model (auto downloads weights)
litgpt pretrain EleutherAI/pythia-160m \
  --tokenizer_dir EleutherAI/pythia-160m \
  --initial_checkpoint_dir EleutherAI/pythia-160m \
  --data TextFiles \
  --data.train_data_path "custom_texts/" \
  --train.max_tokens 10_000_000 \
  --out_dir out/custom-model

# 2) Test the model
litgpt chat out/custom-model/final
```

</details>

[Read the full continued pretraining docs](tutorials/pretrain.md#continued-pretraining-on-custom-data)

&nbsp;

---- 
# Training recipes

LitGPT comes with validated recipes (YAML configs) to train models under different conditions.  We've generated these recipes based on the parameters we found to perform the best for different training conditions.

Browse all training recipes [here](config_hub).

### Example

```bash
litgpt finetune \
  --config https://raw.githubusercontent.com/Lightning-AI/litgpt/main/config_hub/finetune/llama-2-7b/lora.yaml
```
<details>
  <summary>✅ Use configs to customize training</summary>
  
Configs let you customize training for all granular parameters like:

```yaml
# The path to the base model's checkpoint directory to load for finetuning. (type: <class 'Path'>, default: checkpoints/stabilityai/stablelm-base-alpha-3b)
checkpoint_dir: checkpoints/meta-llama/Llama-2-7b-hf

# Directory in which to save checkpoints and logs. (type: <class 'Path'>, default: out/lora)
out_dir: out/finetune/qlora-llama2-7b

# The precision to use for finetuning. Possible choices: "bf16-true", "bf16-mixed", "32-true". (type: Optional[str], default: null)
precision: bf16-true

...
```
</details>

<details>
  <summary>✅ Example: LoRA finetuning config</summary>

&nbsp;

```yaml
# The path to the base model's checkpoint directory to load for finetuning. (type: <class 'Path'>, default: checkpoints/stabilityai/stablelm-base-alpha-3b)
checkpoint_dir: checkpoints/meta-llama/Llama-2-7b-hf

# Directory in which to save checkpoints and logs. (type: <class 'Path'>, default: out/lora)
out_dir: out/finetune/qlora-llama2-7b

# The precision to use for finetuning. Possible choices: "bf16-true", "bf16-mixed", "32-true". (type: Optional[str], default: null)
precision: bf16-true

# If set, quantize the model with this algorithm. See ``tutorials/quantize.md`` for more information. (type: Optional[Literal['nf4', 'nf4-dq', 'fp4', 'fp4-dq', 'int8-training']], default: null)
quantize: bnb.nf4

# How many devices/GPUs to use. (type: Union[int, str], default: 1)
devices: 1

# How many nodes to use. (type: int, default: 1)
num_nodes: 1

# The LoRA rank. (type: int, default: 8)
lora_r: 32

# The LoRA alpha. (type: int, default: 16)
lora_alpha: 16

# The LoRA dropout value. (type: float, default: 0.05)
lora_dropout: 0.05

# Whether to apply LoRA to the query weights in attention. (type: bool, default: True)
lora_query: true

# Whether to apply LoRA to the key weights in attention. (type: bool, default: False)
lora_key: false

# Whether to apply LoRA to the value weights in attention. (type: bool, default: True)
lora_value: true

# Whether to apply LoRA to the output projection in the attention block. (type: bool, default: False)
lora_projection: false

# Whether to apply LoRA to the weights of the MLP in the attention block. (type: bool, default: False)
lora_mlp: false

# Whether to apply LoRA to output head in GPT. (type: bool, default: False)
lora_head: false

# Data-related arguments. If not provided, the default is ``litgpt.data.Alpaca``.
data:
  class_path: litgpt.data.Alpaca2k
  init_args:
    mask_prompt: false
    val_split_fraction: 0.05
    prompt_style: alpaca
    ignore_index: -100
    seed: 42
    num_workers: 4
    download_dir: data/alpaca2k

# Training-related arguments. See ``litgpt.args.TrainArgs`` for details
train:

  # Number of optimizer steps between saving checkpoints (type: Optional[int], default: 1000)
  save_interval: 200

  # Number of iterations between logging calls (type: int, default: 1)
  log_interval: 1

  # Number of samples between optimizer steps across data-parallel ranks (type: int, default: 128)
  global_batch_size: 8

  # Number of samples per data-parallel rank (type: int, default: 4)
  micro_batch_size: 2

  # Number of iterations with learning rate warmup active (type: int, default: 100)
  lr_warmup_steps: 10

  # Number of epochs to train on (type: Optional[int], default: 5)
  epochs: 4

  # Total number of tokens to train on (type: Optional[int], default: null)
  max_tokens:

  # Limits the number of optimizer steps to run (type: Optional[int], default: null)
  max_steps:

  # Limits the length of samples (type: Optional[int], default: null)
  max_seq_length: 512

  # Whether to tie the embedding weights with the language modeling head weights (type: Optional[bool], default: null)
  tie_embeddings:

  #   (type: float, default: 0.0003)
  learning_rate: 0.0002

  #   (type: float, default: 0.02)
  weight_decay: 0.0

  #   (type: float, default: 0.9)
  beta1: 0.9

  #   (type: float, default: 0.95)
  beta2: 0.95

  #   (type: Optional[float], default: null)
  max_norm:

  #   (type: float, default: 6e-05)
  min_lr: 6.0e-05

# Evaluation-related arguments. See ``litgpt.args.EvalArgs`` for details
eval:

  # Number of optimizer steps between evaluation calls (type: int, default: 100)
  interval: 100

  # Number of tokens to generate (type: Optional[int], default: 100)
  max_new_tokens: 100

  # Number of iterations (type: int, default: 100)
  max_iters: 100

# The name of the logger to send metrics to. (type: Literal['wandb', 'tensorboard', 'csv'], default: csv)
logger_name: csv

# The random seed to use for reproducibility. (type: int, default: 1337)
seed: 1337
```
</details>

<details>
  <summary>✅ Override any parameter in the CLI:</summary>

```bash
litgpt finetune \
  --config https://raw.githubusercontent.com/Lightning-AI/litgpt/main/config_hub/finetune/llama-2-7b/lora.yaml \
  --lora_r 4
```
</details>

&nbsp;

----

### License

LitGPT is released under the [Apache 2.0](https://github.com/Lightning-AI/litgpt/blob/main/LICENSE) license.