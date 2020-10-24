# Enhancing Clinical BERT Embedding using a Biomedical Knowledge Base

This repo provides two pretrained models for paper *Enhancing Clinical BERT Embedding using a Biomedical Knowledge Base* by Boran Hao, Henghui Zhu and Ioannis Ch. Paschalidis. The models are originally trained using Tensorflow and has been converted to PyTorch huggingface transformers models.

## Quick tour

To use our pretrained models, download the models from the [release pages](https://github.com/noc-lab/clinical-kb-bert/releases) and unzip them. A sample code for using the models are shown as follows. The code is based on `tranformers==3.3.0` and it should works for tranformers version 3.x. For tranformers version 2.x, you need to change the way to perform tokenization. 

```python
from transformers import AutoModel, AutoTokenizer

model = AutoModel.from_pretrained('./clinical_kb_albert')
tokenizer = AutoTokenizer.from_pretrained('./clinical_kb_albert')

inputs = tokenizer("Hello world!", return_tensors="pt")
outputs = model(**inputs)
```
