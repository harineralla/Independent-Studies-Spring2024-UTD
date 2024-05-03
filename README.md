# Independent-Studies-Spring2024-UTD
### Abstract 

**Bugsplainer** is a novel approach that aims to automatically generate natural language explanations for software bugs, addressing a crucial yet challenging aspect of software development and maintenance. Unlike previous techniques focused solely on bug detection or correction, Bugsplainer leverages advanced transformer models trained on a large dataset of bug-fix commits.

The key innovations of Bugsplainer include its ability to incorporate structural information and identify buggy patterns within the source code, as well as its training approach that exposes the model to both buggy and corrected code versions. This dual training strategy enhances Bugsplainer's understanding of bug characteristics and remediation strategies.

Bugsplainer leverages two key strategies: 1) Utilizing structural information and buggy patterns from the source code to provide context for explanation generation, and 2) Training on both buggy and corrected code versions to enhance its understanding of bug patterns and remediation strategies.

## Comparative Analysis

This study evaluates the effectiveness of Bugsplainer, a state-of-the-art tool for vulnerability detection and fix explanation generation, by comparing its performance on two distinct datasets:

1. **Security Bug Dataset**: A subset of 50 security bugs extracted from the PySecDB dataset, a curated collection of real-world security vulnerabilities in Python codebases.
   Source: https://huggingface.co/datasets/sunlab/PySecDB

3. **Non-Security Bug Dataset**: The test data for non-security bugs is provided with the Bugsplainer tool itself.
   Source: https://github.com/parvezmrobin/bugsplainer-webapp

The analysis aims to assess Bugsplainer's capabilities in handling security vulnerabilities and generating accurate fix explanations, contrasted with its performance on non-security bugs.

### Evaluation Metrics

The comparison is conducted using the following standard evaluation metrics:

- **BLEU** (Bilingual Evaluation Understudy): Measures the similarity between the generated explanations and reference explanations based on n-gram overlap.
- **ROUGE** (Recall-Oriented Understudy for Gisting Evaluation): Evaluates the quality of the generated explanations by comparing them to reference explanations based on n-gram overlap and longest common subsequence.
- **BERT Score**: Computes the similarity between the generated explanations and reference explanations using contextual embeddings from the BERT language model.

### Results
The following shows the Maximum scores achieved by Bugsplainer based on 2 datasets. 

| Metric     | Security Bugs (PySecDB) | Non-Security Bugs (Bugsplainer) |   
|------------|-------------------------|---------------------------------|
| BLEU       | 48.27                   | 57.14                           |    
| ROUGE      | 58.18                   | 63.41                           |   
| BERT Score | 84.44                   | 90.24                           |   


The following shows the Average scores achieved by Bugsplainer based on 2 datasets.
| Metric     | Security Bugs (PySecDB) | Non-Security Bugs (Bugsplainer) |   
|------------|-------------------------|---------------------------------|
| BLEU       | 5.19                    | 23.20                           |    
| ROUGE      | 6.93                    | 28.59                           |   
| BERT Score | 81.63                   | 85.15                           |

Based on the results, it is evident that Bugsplainer's performance is slightly better on its own non-security bug test data compared to the security bugs extracted from PySecDB. The higher scores across all three evaluation metrics for the non-security bug dataset indicate that Bugsplainer generates more accurate and relevant fix explanations for non-security bugs.

However, it's important to note that Bugsplainer still achieves reasonably high scores on the security bug dataset, demonstrating its capability to handle security vulnerabilities as well. The differences in scores between the two datasets are not substantial, suggesting that Bugsplainer can be an effective tool for generating fix explanations, regardless of whether the bug is security-related or not.

These findings highlight the versatility of Bugsplainer and its potential for adoption in various software development and maintenance scenarios, including enhancing the vulnerability detection and remediation processes.
