# Dataset for Query-based Multi-Document Summarization

This repository contains versions of automatically generated datasets for
abstractive and extractive query-based multi-document summarization as described
in [AQuaMuSe paper](https://arxiv.org/pdf/2010.12694.pdf).

High-level Notes:

*   Dependencies: Documents URLs references the
    [Common Crawl June 2017 Archive](https://commoncrawl.org/2017/07/june-2017-crawl-archive-now-available).
*   Data Format:
    *   Directory structure:
        *   Each dataset release with have two top-level folders: `abstractive`
            and `extractive`.
        *   Each top-level folder contains three sub-folders for `train`, `dev`
            and `test` examples.
    *   File format:
        [TFrecords](https://www.tensorflow.org/tutorials/load_data/tfrecord).
    *   Fields:
        *   `query`: input query to be used as summarization context. This is a
            single valued `byte_list` feature, derived from
            [Natural Questions](https://ai.google.com/research/NaturalQuestions/)
            user queries.
        *   `input_urls`: List of URLs to input documents pointing to
            [Common Crawl](https://commoncrawl.org/2017/07/june-2017-crawl-archive-now-available)
            to be summarized. Each URL is separated with a special token
            separator `<EOD>`.
        *   `target`: Summarization target, derived from
            [Natural Questions](https://ai.google.com/research/NaturalQuestions/)
            long answers.

## Disclaimer

This is not an official Google product.

