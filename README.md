# WhatsApp LLM Fine-Tuning Project

This project fine-tunes a large language model (LLM) to emulate a person using their whatsapp chat logs using the [Unsloth](https://github.com/unslothai/unsloth) library and LoRA (Low-Rank Adaptation). It leverages efficient 4-bit quantized models for better performance on limited hardware.

---

## 🚀 Features

- ✅ Fine-tunes 4-bit quantized transformer models  
- ✅ Uses Unsloth for fast, memory-efficient loading  
- ✅ Incorporates LoRA adapters for parameter-efficient training  
- ✅ Configurable for different sequence lengths and data types  

---

## 📦 Requirements

Install the following dependencies:

The notebook installs the following Python packages:

unsloth (via GitHub)

xformers

trl, peft, accelerate, bitsandbytes

Simply run the %%capture portion of the notebook

---

## 🧠 Model Setup
The project uses:

Base model: unsloth/mistral-7b-bnb-4bit

PEFT method: LoRA adapters for efficient fine-tuning

---

## 🛠️ Configuration
Key parameters include:

max_seq_length = 1024

load_in_4bit = True

lora_alpha = 16

r = 16 (LoRA rank)

These can be tuned based on the target application or hardware limitations.


---

## 📝 Usage
Run the whatsapp_llm.ipynb notebook step by step to:

Install necessary packages.

Load the base model.

Apply LoRA adapters.

Export your whatsapp chats merge them into a singular txt file. Concatenating them together will do.

Change person_model to the name of the person you are trying to emulate. (This name must be an exact match to your whatsapp chat log)

Run all in google colab (T4 GPU) or your IDE should you have the appropriate hardware

---

## 📁 Files
whatsapp_llm.ipynb — The main notebook for setup and fine-tuning.
