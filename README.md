# Do the Benefits of Joint Models for Relation Extraction Extend to Document-level Tasks?

This GitLab repository contains the benchmarking code and models for relation extraction tasks. We have evaluated various models, including joint models, NER models plus relation classification models for pipeline approaches, in both sentence-level and document-level settings.

## Joint Models

1. **OneRel**: [GitHub Repository](https://github.com/ssnvxia/OneRel)
2. **BiRTE**: [GitHub Repository](https://github.com/neukg/BiRTE)
3. **GRTE**: [GitHub Repository](https://github.com/neukg/GRTE)
4. **PtrNet**: [GitHub Repository](https://github.com/nusnlp/PtrNetDecoding4JERE)
5. **Rebel**: [GitHub Repository](https://github.com/Babelscape/rebel)

## NER Model

1. **PL-Marker**: [GitHub Repository](https://github.com/thunlp/PL-Marker)

## Relation Classification Models

1. **KD-DocRE**: [GitHub Repository](https://github.com/tonytan48/KD-DocRE)
2. **SAIS**: [GitHub Repository](https://github.com/xiaoyuxin1002/SAIS)
3. **SSAN**: [GitHub Repository](https://github.com/BenfengXu/SSAN)

## Parameter Settings

We used the following parameter settings for our models:

- Document Encoding: BERT_BASE (cased) for all models, except REBEL, for which we used BART_BASE.
- Hardware: NVIDIA Tesla V100 32GB GPU for training.
- Hyper-parameters: We followed the hyper-parameter settings provided in the respective papers of each model.

## Datasets

You can download the NYT and DocRED datasets for all five joint models from [here](https://drive.google.com/drive/folders/1MHzVze0mgp7E8c0zUTLoeJwaxIG3maKA?usp=sharing). Datasets for the NER model PL-Marker are also available at the same link. For the three relation classification models, we have provided the training and validation sets.

To evaluate the end-to-end RE performance, you need to create the test dataset using the output of PL-Marker. The script for creating the test set and obtaining the end-to-end relation extraction results is included with the dataset.
