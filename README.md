🐪 Arabic Text Summarization with TinyLlama + LoRA
📌 Project Overview
This project explores automatic summarization for Arabic text using TinyLlama (1.1B parameters) fine-tuned with LoRA (Low-Rank Adaptation).
The goal is to efficiently adapt a small language model for Arabic summarization using limited resources.

🎯 Objectives
Load and clean the XLSum Arabic dataset
Load TinyLlama-1.1B-Chat model
Fine-tune with LoRA for summarization
Evaluate using ROUGE metrics

📊 Dataset
Dataset: XLSum (Arabic subset)
~60,000 Arabic article-summary pairs

Example:

Article:

شهدت السنوات الأخيرة تطورًا هائلًا في مجال التكنولوجيا...
الحكومة أعلنت عن خطة جديدة لتحسين التعليم في المناطق الريفية...

Summary:

في المقابل، أثارت هذه التغيرات السريعة تحديات عدة تتعلق بالخصوصية الرقمية...
الحكومة تطلق خطة لتطوير التعليم في المناطق الريفية.

🧠 Model & Setup

Base model: TinyLlama/TinyLlama-1.1B-Chat

LoRA: Efficient fine-tuning with minimal memory usage

Quantization: 4-bit (nf4) using bitsandbytes

Libraries:
🤗 Transformers
🤗 PEFT
🤗 TRL
PyTorch

⚙️ Training Details
Batch size: 8
Epochs: 5
Learning rate: 5e-5
Gradient accumulation: 2
Max sequence length: 128 tokens
Fine-tuning method: Supervised Fine-Tuning (SFTTrainer)

📈 Evaluation
Metric: ROUGE (ROUGE-1, ROUGE-2, ROUGE-L)

Results: Model generated concise summaries with acceptable quality
Example output:
Input:
أعلنت وزارة الصحة عن حملة جديدة للتطعيم ضد شلل الأطفال في جميع المحافظات...

Generated Summary:
وزارة الصحة تطلق حملة وطنية للتطعيم ضد شلل الأطفال.

🚀 Challenges
Limited Arabic support in pre-trained LLMs
Prompt understanding in Arabic not always reliable
Hardware/resource constraints

✅ Conclusion
TinyLlama can be adapted efficiently for Arabic NLP with LoRA
Achieved good summarization quality with limited resources
Provides a foundation for other Arabic NLP tasks

🔮 Future Work
Test larger models (e.g., Mistral, Zephyr)
Explore multi-style summarization (concise, long, analytical)
Conduct human evaluation of summaries

📂 Project Structure
📦 arabic-summarization-tinyllama
 ┣ 📜 data_preprocessing.py   # Dataset loading & cleaning
 ┣ 📜 train_lora.py           # Fine-tuning script
 ┣ 📜 evaluate.py             # ROUGE evaluation
 ┣ 📜 requirements.txt        # Dependencies
 ┣ 📜 README.md               # Project overview
 ┗ 📂 results/                # Sample outputs & metrics

⚡ Installation & Usage
1. Clone repo
git clone https://github.com/BatoulHamdan/arabic-summarization.git
cd arabic-summarization

2. Install dependencies
pip install -r requirements.txt

3. Run training
python train_lora.py

4. Run evaluation
python evaluate.py

🙌 Acknowledgments
XLSum dataset
TinyLlama model
Hugging Face libraries: Transformers, PEFT, TRL

🔥 If you like this project, feel free to star ⭐ the repo and connect with me on LinkedIn.
