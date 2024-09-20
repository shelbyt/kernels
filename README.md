## Getting started

* Install dependencies

```bash
python3 -m pip install triton fairscale fire torch tiktoken blobfile huggingface_hub[cli]
```

* Download llama model

```bash
export HF_TOKEN=xxx

huggingface-cli download meta-llama/Meta-Llama-3-8B-Instruct \
--local-dir $HOME/models/llama-3-8b-instruct \
--local-dir-use-symlinks False
```

* Clone repo and get branch

```bash
git clone https://github.com/shelbyt/kernels.git
cd kernel
git checkout cudamode
python3 test_llama.py
```
