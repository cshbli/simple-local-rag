## Create one virtual environment
```
conda create -n rag python=3.11
```

### Install requirements
```
pip install -r requirements.txt
```

after that, install flash-attn
```
pip install flash-attn
```

- Change the SentenceTransformer from `cpu` to `cuda`

```
embedding_model = SentenceTransformer(model_name_or_path="all-mpnet-base-v2", 
                                      device="cuda") # choose the device to load the model to (note: GPU will often be *much* faster than CPU)
```                                      

### Hugging Face login
```
from huggingface_hub import login
login()
```