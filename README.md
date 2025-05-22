---
license: MIT
---

# Dataset Card for Hmar Bible Dataset

This dataset contains parallel verses in English and Hmar languages, curated from the **American Standard Version (ASV)** for English and the **Christian Literature by Bible Society of India (CLBSI)** for Hmar. It is structured to facilitate linguistic and translation studies.

## Dataset Details

### Dataset Description

This dataset provides verse-level parallel translations of the Bible in English (ASV) and Hmar (CLBSI). Each book is saved as a separate CSV file with the structure:  

| en                          | hmr                          |
|-----------------------------|------------------------------|
| "In the beginning..."       | "A tîrin Pathienin hnuoi..." |

- **Curated by:** Hmar_Lang  
- **Language(s) (NLP):** English, Hmar  
- **License:** CC-BY-4.0  

### Dataset Sources

- **Repository:** [Hmar Bible Dataset on Huggingface](https://huggingface.co/datasets/hmar-lang/hmar-bible-dataset)
- **Paper [optional]:** N/A  
- **Demo [optional]:** N/A  

## Uses

### Direct Use

This dataset can be used for:  
1. Linguistic analysis and translation studies.  
2. Training or fine-tuning multilingual and low-resource language models.  
3. Cross-language information retrieval tasks.  

### Out-of-Scope Use

1. The dataset is not suitable for non-academic or commercial purposes that violate the licensing agreement.  
2. It is not recommended for tasks requiring contextual annotations, as it only includes raw verses.  

## Dataset Structure

The dataset consists of separate CSV files for each book of the Bible, named as `<Book_Name>.csv` (e.g., `Genesis.csv`).  

- **Columns:**  
  - `en`: Verse content in English from ASV.  
  - `hmr`: Verse content in Hmar from CLBSI.  

Example CSV structure for `Genesis.csv`:  

| en                           | hmr                           |
|------------------------------|-------------------------------|
| "In the beginning..."        | "A tîrin Pathienin hnuoi..."  |
| "And the earth was..."       | "Chun, hnuoi hi a sie..."     |

### Corrections

During dataset creation, mismatched rows between the ASV Bible and CLBSI Bible were identified and corrected. The discrepancies were found in the following books:  

1. **3 John:** ASV contains 14 verses, while CLBSI contains 15 verses.  
2. **Ephesians:** ASV contains 155 verses, while CLBSI contains 154 verses.  
3. **Revelation:** ASV contains 404 verses, while CLBSI contains 405 verses.  

These mismatches were manually reviewed and resolved to ensure alignment in the final dataset.

### Observations

The translations, while attempting to be literal, cannot achieve a 100% word-for-word alignment due to inherent grammatical and linguistic differences between English and Hmar. The dataset reflects these nuances and captures the intended meaning as closely as possible.

## Dataset Creation

### Curation Rationale

The dataset was created to promote the preservation of the Hmar language and to facilitate linguistic studies and translation model development for low-resource languages.

### Source Data

#### Data Collection and Processing

- **Source:** The English data was collected from the ASV Bible, and the Hmar data was collected from the CLBSI Bible.  
- **Processing:** JSON files containing verses were parsed and matched on a verse-by-verse basis to create CSV files for each book.  

#### Who are the source data producers?

The original texts are authored and compiled by:  
1. The ASV Bible Committee.  
2. Christian Literature by Bible Society of India (CLBSI).  

### Annotations

No additional annotations were made. The dataset consists solely of raw verse content.  

#### Personal and Sensitive Information

This dataset does not contain personal or sensitive information. It includes only publicly available religious texts.  

## Bias, Risks, and Limitations

1. **Bias:**  
   - Translational differences between ASV and CLBSI may introduce semantic mismatches.  
   - Cultural and doctrinal differences may influence the translations.  

2. **Technical Limitations:**  
   - Limited to verse-level translations. Contextual analysis may require additional data.  
   - Verses in ASV and Hmar may not always align perfectly due to structural differences in the source texts.  

## Recommendations

Users should ensure appropriate preprocessing and validation before using the dataset for critical applications.

# Related Datasets
- [Hmar Language Basic Words on Huggingface](https://huggingface.co/datasets/hmar-lang/hmar-language-basic-words)
- [Hmar Language Conversations on Huggingface](https://huggingface.co/datasets/hmar-lang/hmar-language-conversations)

## Citation

**BibTeX:**
```bibtex
@dataset{asv_clbsi_bible,
  title = {Hmar Bible Dataset},
  author = {Hmar Language Dataset Project},
  year = {2024},
  publisher = {https://huggingface.co/datasets/hmar-lang/Hmar-Bible-Dataset},
  license = {CC-BY-4.0}
}

Glossary

ASV: American Standard Version of the Bible.

CLBSI: Christian Literature by Bible Society of India.


More Information

For more details, contact: pheklom@gmail.com

Dataset Card Authors

Hmar Language Dataset Project 

Dataset Card Contact

pheklom@gmail.com
