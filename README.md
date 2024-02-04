# Topsis for pre-trained LLMs
TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) is performed on pre-trained models for evaluating their performance on text summarization considering various parameters.

## Models
All the models used are sourced from [Hugging face](https://huggingface.co).
1. [facebook/bart-large-cnn](https://huggingface.co/facebook/bart-large-cnn)
2. [philschmid/bart-large-cnn-samsum](https://huggingface.co/philschmid/bart-large-cnn-samsum)
3. [google/pegasus-cnn_dailymail](https://huggingface.co/google/pegasus-cnn_dailymail)
4. [sshleifer/distilbart-cnn-12-6](https://huggingface.co/sshleifer/distilbart-cnn-12-6)

## Parameters for evaluation
1. **BERT Score** : leverages pre-trained language models like BERT (Bidirectional Encoder Representations from Transformers) to calculate semantic similarity between a generated text and its reference counterpart.
  
   It consists of Precision, Recall and F1-score.
   
2. **BLEU Score (Bi-Lingual Evaluation Understudy)** : measures n-gram overlaps between a generated text and reference texts.
3. **METEOR Score (Metric for Evaluation of Translation with Explicit Ordering)** : combines elements of BLEU and ROUGE by considering n-gram precision, recall, and word order similarity.

## Final Output
Models | Precision | Recall | F1 Score | METEOR | BLEU | Topsis Score | Rank
--- | --- | --- | --- |--- |--- |--- |--- 
M1 | 0.845326 | 0.48746 | 0.618348 | 0.099406 | 0.000768 | 0.291483 | 3
M2 | 0.800241 | 0.53049 | 0.638025 | 0.125424 | 0.003623 | 1.000000 | 1
M3 | 0.790937 | 0.449346 | 0.573102 | 0.05382 | 0.00001 | 0.000000 | 4
M4 | 0.856211 | 0.50466 | 0.635028 | 0.112289 | 0.001518 | 0.475114 | 2

## Best Model
M2 : [philschmid/bart-large-cnn-samsum](https://huggingface.co/philschmid/bart-large-cnn-samsum)
