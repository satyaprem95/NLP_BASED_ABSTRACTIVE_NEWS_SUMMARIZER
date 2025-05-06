# NLP_BASED_ABSTRACTIVE_NEWS_SUMMARIZER

## Problem Statement

Sure! Here's the problem statement in a single line:

"Automating the process of summarizing lengthy textual content to make information more accessible and digestible."

The rapid growth of digital content has resulted in an overwhelming amount of textual information across various platforms. Manually summarizing lengthy documents, news articles, and reports is a time-consuming task. Therefore, there is a growing need for automated systems that can generate concise and meaningful summaries of long text, making the information easier to understand and digest. This project aims to build an automated text summarization pipeline that can generate high-quality summaries from long articles or documents, focusing on **abstractive summarization**, where the model generates new sentences rather than simply extracting parts of the original text.

## Hugging Face Pre-trained Model

For this project, the **T5-small** model from Hugging Face’s `transformers` library is used. T5 (Text-To-Text Transfer Transformer) is a powerful model designed to handle a wide range of NLP tasks, including text summarization, by converting each task into a text-to-text problem. 

The model then generates a natural-language summary based on this input. The `T5-small` version was chosen for this project due to its balance between performance and computational efficiency, making it suitable for experimenting in environments such as Google Colab and Kaggle. By using a pre-trained model from Hugging Face, we significantly reduce the need for extensive training from scratch, leveraging the knowledge the model has already learned from large text corpora.

## Performance Metrics

To evaluate the performance of the model, we have used two widely adopted metrics in the text summarization domain:

* **ROUGE (Recall-Oriented Understudy for Gisting Evaluation)**: A set of metrics for evaluating automatic summarization by comparing the overlap of n-grams, word sequences, and word pairs between the generated summary and a reference summary. We mainly use ROUGE-N (for n-grams) and ROUGE-L (for longest common subsequence).

* **BERTScore**: A metric based on BERT embeddings to measure the semantic similarity between the generated summary and the reference summary. Unlike ROUGE, BERTScore evaluates the quality of the generated summary at the semantic level rather than relying on surface-level n-gram overlap.

## General Use Case

Although this project has been primarily tested on the **news domain** (using the CNN/DailyMail dataset), the approach is not limited to news articles. The model can be adapted for summarizing various types of text, including:

* Academic papers
* Reports
* Legal documents
* Blogs
* Social media posts
* Technical documentation

With minimal adjustments to the data preprocessing pipeline, this text summarization model can be applied to a wide range of summarization tasks across different domains.

## Conclusion

This project demonstrates the power and flexibility of the T5 model for automatic text summarization. By utilizing the Hugging Face pre-trained model, we are able to quickly and efficiently generate high-quality summaries with minimal effort. The use of evaluation metrics like ROUGE and BERTScore ensures that the model's performance is accurately assessed, making it a robust solution for a variety of summarization purposes.

