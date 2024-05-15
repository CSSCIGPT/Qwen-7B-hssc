# CSSCIGPT



## 介绍

基于1998-2023年间的CSSCI标题和摘要及部分人文社会科学学术全文本，课题组使用阿里巴巴推出的多语种开源大模型之一的Qwen作为基座模型，构建了人文社科领域中文大语言模型CSSCIGPT，并通过人文社科领域术语分类下游任务验证模型效果，结果显示，人文社科垂直领域模型在处理领域性较强的相关问题上表现出了良好性能，为人文社科领域与大模型技术的集合提供了基础工具。



## 使用方法

### Huggingface Transformers

基于Huggingface Transformers的from_pretrained方法可以直接在线获取CSSCIGPT模型。

```python
from transformers import AutoModelForCausalLM, AutoTokenizer
device = "cuda" # the device to load the model onto

model = AutoModelForCausalLM.from_pretrained(
    "KM4STfulltext/CSSCIGPT",
    torch_dtype="auto",
    device_map="auto"
)
tokenizer = AutoTokenizer.from_pretrained("KM4STfulltext/CSSCIGPT")
```




