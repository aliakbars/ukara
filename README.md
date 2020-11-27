# Knowing Right from Wrong - Should We Use More Complex Models for Automatic Short-Answer Scoring in Bahasa Indonesia?

Authors: [Ali Akbar Septiandri](https://twitter.com/aliakbars), [Yosef Ardhito Winatmoko](https://twitter.com/yoseflaw), [Ilham Firdausi Putra](https://twitter.com/ilhamfp31)

**To appear in [SustaiNLP](https://sites.google.com/view/sustainlp2020) workshop at [EMNLP 2020](https://2020.emnlp.org/)**

![](https://nlp.mipa.ugm.ac.id/wp-content/uploads/sites/888/2019/07/UKARA-LOGO-800X-218-300x82.png)

From the website:
> Ukara is a web-based  automatic short answer scoring system which is a collaboration project between our group and PUSPENDIK, Ministry of Education and Culture of Indonesia. The name is originally from Javanese language which means a sentence. The system was built based on supervised machine learning approach which is able to assign a score to student’s answer. The student’s answer usually consists of maximum 2-3 sentences. The project is still going on with the aim to improve Ukara’s performance.

We compare three solutions to [UKARA 1.0 challenge](https://nlp.mipa.ugm.ac.id/ukara-1-0-challenge/) on automated short-answer scoring: single classical, ensemble classical, and deep learning. The task is to classify given answers to two questions, whether they are right or wrong. While recent development shows increasing model complexity to push the benchmark performances, they tend to be resource-demanding with mundane improvement. For the UKARA task, we found that bag-of-words and classical machine learning approaches can compete with ensemble models and Bi-LSTM model with pre-trained word2vec embedding from 200 million words. In this case, the single classical machine learning achieved less than 2% difference in F1 compared to the deep learning approach with 1/18 time for model training.

## Model Performance

F1 score comparison with the alternative ensemble models
| Model                |   Train A |   Train B |   Dev |   Test |
|:---------------------|----------:|----------:|------:|-------:|
| Single               |     0.892 |     0.768 | 0.793 |  0.8   |
| Ensemble + Original  |     0.885 |     0.764 | 0.799 |  0.802 |
| Ensemble + Corrected |     0.898 |     0.831 | 0.802 |  0.804 |
| Deep Learning        |     0.9   |     0.772 | 0.806 |  0.811 |

## Required Resource

Total training time for each method (in minutes)
| Model                | Word2Vec   |   Task A |   Task B |   Total |
|:---------------------|:-----------|---------:|---------:|--------:|
| Single               | -          |     8.98 |    10.07 |   19.05 |
| Ensemble + Original  | -          |    36.53 |    36.07 |   73.23 |
| Ensemble + Corrected | -          |    44.45 |    45.78 |   90.23 |
| Deep Learning        | 79.15      |   132.42 |   132.06 |  343.63 |

## Acknowledgement

The authors would like to thank the [Natural Language Processing Group of Universitas Gadjah Mada](https://nlp.mipa.ugm.ac.id/) and PUSPENDIK, Ministry of Education and Culture of Indonesia for providing the dataset and organizing challenge. The authors also very much appreciate the reviewers for constructive feedback.

## Citing This Work

```
@inproceedings{septiandri-etal-2020-knowing,
    title = "Knowing Right from Wrong: Should We Use More Complex Models for Automatic Short-Answer Scoring in {B}ahasa {I}ndonesia?",
    author = "Septiandri, Ali Akbar  and
      Winatmoko, Yosef Ardhito  and
      Putra, Ilham Firdausi",
    booktitle = "Proceedings of SustaiNLP: Workshop on Simple and Efficient Natural Language Processing",
    month = nov,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.sustainlp-1.1",
    pages = "1--7",
}
```
