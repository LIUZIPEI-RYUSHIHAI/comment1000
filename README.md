# Comment1000: A Multi-Dimensional Sarcasm Dataset for Chinese Social Media
This is our open dataset for SinoSarcasmClassifier: A Multi-View Model for Sarcasm Detection in Chinese Social Media with Emoji Mapping paper

**Comment1000** is a manually annotated dataset of 17,030 Chinese Weibo comments, designed to support the study and modeling of sarcasm in Chinese social media. The dataset captures sarcasm across multiple linguistic and semantic dimensions, including textual patterns, emoji use, polarity inversion, and syntactic cues.

## Dataset Overview

- Language: Chinese  
- Source: Public Weibo comments  
- Size: 17,030 entries  
- Annotation: Manual, with full agreement between two native Chinese speakers  
- Purpose: Sarcasm detection and multi-dimensional sarcasm analysis  

To reflect the compositional nature of sarcasm, the dataset is divided into four subsets, each corresponding to a specific module designed to model a key aspect of sarcastic expression.

## File Descriptions

The dataset consists of the following CSV files:

### 1. `1000_for_test.csv`

- A testing-oriented subset of 1,000 comments and this is why we called our dataset : comment1000.
- Contains basic annotations along with automatic analysis results.
- Includes outputs from tools such as SnowNLP, for auxiliary experiments or benchmarking.

### 2. `emoji_comments.csv`

- Contains comments that include emojis.
- Intended for studying the role of emoji semantics and emoji-text interactions in sarcasm detection.
- Each entry includes a sarcasm label and additional metadata.

### 3. `puretext_comments.csv`

- Contains comments without any emojis.
- Serves as a contrast set for isolating pure textual sarcastic cues without multimodal elements.

## Field Definitions

All `.csv` files share a basic structure, with at least the following core fields:

- `comment`: The original Weibo comment text in Chinese.
- `irony`: Binary sarcasm label.
  - `1`: The comment contains sarcasm.
  - `0`: The comment does not contain sarcasm.

Other fields (depending on the file) may include:

- `snowNLP_score`: Sentiment score computed using the SnowNLP toolkit.
- ...

These fields are used for analysis or feature extraction and may vary across subsets.


## License

This dataset is released under the [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/) license.
Commercial use is strictly prohibited.
