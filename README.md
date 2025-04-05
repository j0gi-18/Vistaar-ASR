# Vistaar-ASR
This repository evaluates the Whisper Hindi speech-to-text model on the Kathbath dataset. The model is trained using the Whisper framework and is designed to recognize Hindi speech. The evaluation script uses the evaluation.py file to test the model on the Kathbath dataset.

# Setup
1. Clone the repository using git clone https://github.com/AI4Bharat/vistaar.git.
2. Install the required packages by running sudo apt install ffmpeg and pip install -r /content/vistaar/requirements.txt.
3. Navigate to the repository directory using cd /content/vistaar.

# Download Dataset
1. Download the Kathbath dataset using wget https://objectstore.e2enetworks.net/indic-asr-public/indicwhisper/vistaar_benchmarks/kathbath.zip.
2. Download the Whisper Hindi model using wget https://objectstore.e2enetworks.net/indic-asr-public/indicwhisper/all_lang_models/hindi_models.zip.
3. Download the Gramvaani dataset using wget https://asr.iitm.ac.in/Gramvaani/NEW/GV_Eval_3h.tar.gz.

# Evaluation
1. Unzip the downloaded files using unzip kathbath.zip, unzip hindi_models.zip, and tar -xf GV_Eval_3h.tar.gz.
2. Run the evaluation script using python evaluation.py with the following arguments:


```bash
python evaluation.py \
  --model_path /path/to/whisper-hindi-model \
  --manifest_path /path/to/kathbath/manifest.json \
  --manifest_name manifest \
  --device GPU/or/CPU \
  --batch_size 8 \
  --language Hindi/or/other/language
```

# Output
The evaluation script outputs the model's performance metrics, including the character error rate (CER): 3.76% and word error rate (WER): 10.42% with the time taken for evaluation, 56 min.

