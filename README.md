# Minutes Item Segmentation

This repository hosts the files from
[Yuhao Zhuang](https://github.com/Yuhao-Zhuang-gif),
[Eva Maxfield Brown](https://github.com/evamaxfield),
and [Nic Weber's](https://github.com/nniiicc)
collaboration in Winter 2023.

The aim of this work was to experiment with various methods for generating and
aligning minutes items to their associated transcript.

For more information as the project and the results, please see:
[paper.pdf](./paper.pdf).

## Results

After spending time learning about possible solutions to minutes item generation
or alignment, we ultimately decided that any problem we attempted to solve was missing
a dataset for evaluation our algorithm or model.

The resulting dataset (`cdp-minutes-item-seg.json`) is the start of such a dataset.
It contains 27 human created segmentations for meetings of the Seattle City Council
using data from the [Council Data Project](https://github.com/CouncilDataProject).

The major takeaways from this work include:

*   A starting point from which to continue building a larger
    (more complete and "accurate") dataset.
*   Observations about the difficult of "accurate" segmentation,
    specifically in our case due to the following reasons:
    *   Some minutes are not explicitely mentioned in meeting transcripts
    *   In actual meetings, certain minutes items are combined instead of discussed one
        at a time

## Notes

Only Seattle City Council meetings are included in this example dataset.
The "id" for each segmentation string is the event id as it is made available from CDP.

## Other Files

The `semantic_dtw_sentences_and_minutes_and_evaluation.ipynb` notebook uses the dataset
to evaluate a simple semantic dynamic time warping algorithm.

The `archive` directory stores files which were used earlier in the quarter while we were
still experimenting and learning various methods.

