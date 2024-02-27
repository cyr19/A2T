# A2T

We release now the data collected for our paper: [Transformers Go for the LOLs: Generating (Humourous) Titles from Scientific Abstracts End-to-End](https://arxiv.org/abs/2212.10522).

> **Abstract**: 
> We consider the end-to-end abstract-to-title
generation problem, exploring seven recent
transformer based models (including ChatGPT)
fine-tuned on more than 30k abstract-title pairs
from NLP and machine learning (ML) venues.
As an extension, we also consider the harder
problem of generating humorous paper titles.
For the latter, we compile the first large-scale
humor annotated dataset for scientific papers
in the NLP/ML domains, comprising ∼2.6k
titles. We evaluate all models using human
and automatic metrics. Our human evaluation
suggests that our best end-to-end system performs similarly to human authors (but arguably
slightly worse). Generating funny titles is more
difficult, however, and our automatic systems
clearly underperform relative to humans and
often learn dataset artefacts of humor. Finally,
ChatGPT, without any fine-tuning, performs on
the level of our best fine-tuned system.

The data for **abstract-to-title generation** is located in the [`eval_anno_data/`](eval_anno_data/) folder.
* [`2638_humor_annotated_no_squibs.csv`](eval_anno_data/2638_humor_annotated_no_squibs.csv): human annotations regarding humor levels of titles.
* [`32952_with_humor_label_no_squibs.csv`](eval_anno_data/32952_with_humor_label_no_squibs.csv): all abstract-title pairs with human/automatic annotations for humor.
  * [`train_no_squibs.csv`](eval_anno_data/train_no_squibs.csv): train set
  * [`dev_no_squibs.csv`](eval_anno_data/train_no_squibs.csv): dev set
  * [`test_no_squibs.csv`](eval_anno_data/test_no_squibs.csv): test set
* [`dataset_230samples.json`](eval_anno_data/dataset_230samples.json): human evaluation for title generation.
* [`eval_1_processed.csv`](eval_anno_data/eval_1_processed.csv): human evaluation for humorous title generation (BARTXsum vs. BARTXsum-psuedo).
* [`eval_2_processed.csv`](eval_anno_data/eval_2_processed.csv): human evaluation for humorous title generation (BARTXsum vs. ChatGPT).


The data for **abstract+x-to-title generation** is located in the [`long_input/`](long_input/) folder.
* [`data/`](long_input/data): Titles paired with abstract, introduction and conclusion:
  * [`train.json`](long_input/data/train.json): train set
  * [`dev.json`](long_input/data/dev.json): dev set
  * [`test.json`](long_input/data/test.json): test set
  * [`anno/`](long_input/data/anno): human evaluation
* [`models/`](long_input/models): training args for each model with predictions on the test set.

 
If you use the data from this work, please cite us!
```bigquery
@inproceedings{chen2023transformers,
      title={Transformers Go for the LOLs: Generating (Humourous) Titles from Scientific Abstracts End-to-End}, 
      author={Yanran Chen and Steffen Eger},
      year={2023},
      booktitle={Eval4NLP}
}
```

If you're interested in the data that hasn't been uploaded, you could also drop me a line: [yanran.chen@uni-mannheim.de](mailto:yanran.chen@uni-mannheim.de).
