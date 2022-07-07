# MultiNERD

Data and evaluation code for the paper [MultiNERD: A Multilingual, Multi-Genre and Fine-Grained Dataset for Named Entity Recognition (and Disambiguation)](https://www.researchgate.net/publication/361795554_MultiNERD_A_Multilingual_Multi-Genre_and_Fine-Grained_Dataset_for_Named_Entity_Recognition_and_Disambiguation).

```bibtex
@inproceedings{tedeschi-etal-2022-multinerd,
    title = "MultiNERD: A Multilingual, Multi-Genre and Fine-Grained Dataset for Named Entity Recognition (and Disambiguation)",
    author = "Tedeschi, Simone and Navigli, Roberto",
    booktitle = "Findings of the Association for Computational Linguistics: NAACL 2022",
    month = jul,
    year = "2022",
    address = "Seattle, Washington",
    publisher = "Association for Computational Linguistics",
}
```

**Please consider citing our work if you use data and/or code from this repository.**

In a nutshell, MultiNERD is the first **language-agnostic** methodology for automatically creating **multilingual, multi-genre and fine-grained annotations** for **Named Entity Recognition** and **Entity Disambiguation**. Specifically, it can be seen an extension of the combination of two prior works from our research group that are [WikiNEuRal](https://www.github.com/Babelscape/wikineural), from which we took inspiration for the state-of-the-art silver-data creation methodology, and [NER4EL](https://www.github.com/Babelscape/NER4EL), from which we took the fine-grained classes and inspiration for the entity linking part. 

The produced dataset covers:
- **10 languages**: Chinese, Dutch, English, French, German, Italian, Polish, Portuguese, Russian and Spanish;
- **15 NER categories**: Person (PER), Location (LOC), Organization (ORG}), Animal (ANIM), Biological entity (BIO), Celestial Body (CEL), Disease (DIS), Event (EVE), Food (FOOD), Instrument (INST), Media (MEDIA), Plant (PLANT), Mythological entity (MYTH), Time (TIME) and Vehicle (VEHI);
- **2 textual genres**, i.e. [Wikipedia](https://www.wikipedia.org/) and [WikiNews](https://www.wikinews.org/) articles;
- **3 different reference KBs for entity disambiguation**, i.e. [BabelNet](https://babelnet.org/), [WikiData](https://www.wikidata.org) and [Wikipedia](https://www.wikipedia.org/). 

Additionally, we included image URLs to encourage the creation of **multimodal** systems.

Finally, MultiNERD shows consistent improvements of up to **against state-of-the-art alternative** data production methods on common benchmarks for NER while covering a broader set of NER categories (15 vs. 4):

![comparison](img/coarse_results.png)

<br>

# Data

| Dataset Version | Sentences | Tokens | PER | ORG | LOC | ANIM | BIO | CEL | DIS | EVE | FOOD | INST | MEDIA | MYTH | PLANT | TIME | VEHI | OTHER |
| :------------- | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: | -------------: |
| [MultiNERD EN](./data/multinerd_en.tsv) | 164.1K | 3.6M | 75.8K | 33.7K | 78.5K | 15.5K | 0.2K | 2.8K | 11.2K | 3.2K | 11.0K | 0.4K | 7.5K | 0.7K | 9.5K | 3.2K | 0.5K | 3.1M |
| [MultiNERD ES](./data/multinerd_es.tsv) | 173.2K | 4.3M | 70.9K | 20.6K | 90.2K | 10.5K | 0.3K | 2.4K | 8.6K | 6.8K | 7.8K | 0.6K | 8.0K | 1.6K | 7.6K | 45.3K | 0.3K | 3.8M |
| [MultiNERD NL](./data/multinerd_nl.tsv) | 171.7K | 3.0M | 56.9K | 21.4K | 78.7K | 34.4K | 0.1K | 2.1K | 6.1K | 4.7K | 5.6K | 0.2K | 3.8K | 1.3K | 6.3K | 31.0K | 0.4K | 2.7M |
| [MultiNERD DE](./data/multinerd_de.tsv) | 156.8K | 2.7M | 79.2K | 31.2K | 72.8K | 11.5K | 0.1K | 1.4K | 5.2K | 4.0K | 3.6K | 0.1K | 2.8K | 0.8K | 7.8K | 3.3K | 0.5K | 2.4M |
| [MultiNERD RU](./data/multinerd_ru.tsv) | 129.0K | 2.3M | 43.4K | 21.5K | 75.2K | 7.3K | 0.1K | 1.2K | 1.9K | 2.8K | 3.2K | 1.1K | 11.3K | 0.6K | 4.8K | 22.8K | 0.5K | 2.0M |
| [MultiNERD IT](./data/multinerd_it.tsv) | 181.9K | 4.7M | 75.3K | 19.3K | 98.5K | 8.8K | 0.1K | 5.2K | 6.5K | 5.8K | 5.8K | 0.8K | 8.6K | 1.8K | 5.1K | 71.2K | 0.6K | 4.2M |
| [MultiNERD FR](./data/multinerd_fr.tsv) | 176.2K | 4.3M | 89.6K | 28.2K | 90.9K | 11.4K | 0.1K | 2.3K | 3.1K | 7.4K | 3.2K | 0.7K | 8.0K | 2.0K | 4.4K | 27.4K | 0.6K | 3.8M |
| [MultiNERD PL](./data/multinerd_pl.tsv) | 195.0K | 3.0M | 66.5K | 29.2K | 100.0K | 19.7K | 0.1K | 3.3K | 6.5K | 6.7K | 3.3K | 0.6K | 4.9K | 1.3K | 6.6K | 44.1K | 0.7K | 2.5M |
| [MultiNERD PT](./data/multinerd_pt.tsv) | 177.6K | 3.9M | 54.0K | 13.2K | 124.8K | 14.7K | 0.1K | 4.2K | 6.8K | 5.9K | 5.4K | 0.6K | 9.1K | 1.6K | 9.2K | 48.6K | 0.3K | 3.4M |
| [MultiNERD ZH](./data/multinerd_zh.tsv) | 115.0K | 2.4M | 47.7K | 22.2K | 70.4K | 6.9K | 0.1K | 1.4K | 2.2K | 2.5K | 2.9K | 0.5K | 6.9K | 0.7K | 5.2K | 27.4K | 0.4K | 2.1M |


We remark that the datasets are automatically created, and, therefore, they may contain errors. 

<br>



# License 
MultiNERD is licensed under the CC BY-SA-NC 4.0 license. The text of the license can be found [here](./LICENSE).

We underline that the source from which the raw sentences have been extracted are Wikipedia ([wikipedia.org](https://www.wikipedia.org/)) and Wikinews [wikinews.org](https://www.wikinews.org/) and the NER annotations have been produced by [Babelscape](https://babelscape.com/).

<br>

# Acknowledgments
We gratefully acknowledge the support of the **ERC Consolidator Grant MOUSSE No. 726487** under the European Union’s Horizon2020 research and innovation programme ([http://mousse-project.org/](http://mousse-project.org/)).