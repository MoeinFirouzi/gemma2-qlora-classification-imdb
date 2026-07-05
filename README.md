# Fine-Tuning Gemma-2-2B with LoRA for IMDB Sentiment Classification

This project demonstrates how to fine-tune **Gemma-2-2B** for binary sentiment classification on the IMDB movie reviews dataset using **Parameter-Efficient Fine-Tuning (PEFT)**. We apply **LoRA (Low-Rank Adaptation)** to train only a small subset of parameters, combined with **4-bit quantization (QLoRA)** to enable efficient training under limited GPU resources.

The workflow includes dataset loading, preprocessing, tokenization, model quantization, LoRA configuration, supervised fine-tuning using the Hugging Face Trainer API, and evaluation using standard classification metrics. The trained model is then used for inference on unseen movie reviews.

This work is based on the **Gemma 2 model family released by Google**, and follows its usage requirements and license terms. Gemma 2 models are provided under Google’s usage guidelines, which emphasize responsible AI use, compliance with the acceptable use policy, and restrictions on deploying the model in unsafe or disallowed applications. Users should ensure they review and follow the official Gemma 2 license before deploying or redistributing the model.

## Related Papers

This project is inspired by the following key works:

- **LoRA: Low-Rank Adaptation of Large Language Models** Hu et al., 2021.  
  Introduces Low-Rank Adaptation (LoRA), a parameter-efficient fine-tuning method that freezes the pre-trained model weights and injects trainable low-rank matrices into each layer.  
  [DOI: 10.48550/arXiv.2106.09685](https://doi.org/10.48550/arXiv.2106.09685)

- **QLoRA: Efficient Finetuning of Quantized LLMs** Dettmers et al., 2023.  
  Proposes fine-tuning large language models in 4-bit precision using quantization and LoRA, enabling training of very large models on limited hardware.  
  [DOI: 10.48550/arXiv.2305.14314](https://doi.org/10.48550/arXiv.2305.14314)

- **Attention Is All You Need** Vaswani et al., 2017.  
  Introduces the Transformer architecture, which is the foundation of modern large language models including Gemma 2.  
  [DOI: 10.48550/arXiv.1706.03762](https://doi.org/10.48550/arXiv.1706.03762)

- **Gemma 2: Improving Open Language Models at a Practical Size** Gemma Team, Google DeepMind, 2024.  
  Presents the Gemma 2 family of lightweight, state-of-the-art open models, introducing architectural updates such as interleaved local-global attention, grouped-query attention, and knowledge distillation for smaller model scales.  
  [DOI: 10.48550/arXiv.2408.00118](https://doi.org/10.48550/arXiv.2408.00118)

- **IMDB Dataset of Movie Reviews** Maas et al., 2011.  
  A widely used benchmark dataset for binary sentiment classification tasks.  
