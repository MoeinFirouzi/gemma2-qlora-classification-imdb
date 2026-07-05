# Fine-Tuning Gemma2-2B with QLoRA for IMDB Sentiment Classification

This project demonstrates how to fine-tune **Gemma2-2B** for binary sentiment classification on the IMDB movie reviews dataset using **Parameter-Efficient Fine-Tuning (PEFT)**. We apply **LoRA (Low-Rank Adaptation)** to train only a small subset of parameters, combined with **4-bit quantization (QLoRA)** to enable efficient training under limited GPU resources.

The workflow includes dataset loading, preprocessing, tokenization, model quantization, LoRA configuration, supervised fine-tuning using the Hugging Face Trainer API, and evaluation using standard classification metrics. The trained model is then used for inference on unseen movie reviews.

This work is based on the **Gemma model family released by Google**, and follows its usage requirements and license terms. Gemma models are provided under Google’s usage guidelines, which emphasize responsible AI use, compliance with the acceptable use policy, and restrictions on deploying the model in unsafe or disallowed applications. Users should ensure they review and follow the official Gemma license before deploying or redistributing the model.
