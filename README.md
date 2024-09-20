python3 -m pip install triton fairscale fire torch tiktoken blobfile huggingface_hub[cli]

huggingface-cli download meta-llama/Meta-Llama-3-8B-Instruct \
--local-dir $HOME/models/llama-3-8b-instruct \
--local-dir-use-symlinks False

export HF_TOKEN=xxx

git clone https://github.com/shelbyt/kernels.git
cd kernels
git checkout cudamode

python3 test_llama.py
