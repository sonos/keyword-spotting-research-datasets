# keyword-spotting-research-datasets

## Overview

### Reference

This repository contains the license and instructions relative to the open
Data Sets mentioned in this publication:

```
Coucke et al., 2018, "Efficient keyword spotting using dilated convolutions
and gating"
```

[link]

A different version was used in [Leroy et al., 2018, "Federated learning for
keyword spotting"](https://arxiv.org/abs/1810.05512). Please mention which
version you want access to in your contact email (see below).

### Data Set

The wake word is "Hey Snips" pronounced with no pause between the two
words.
The Data Set contains a large variety of English accents and recording
environments. Around 11K wake word utterances and 86.5K (~23 hours)
negative examples have been recorded. Note that negative samples have been
recorded in the same conditions than wake-word utterances, therefore arising
 from the same domain (speaker, hardware, environment, etc.).

Positive data has been cleaned by automatically removing samples of extreme
duration (1st and 99th percentiles), or samples with repeated occurrences of
the wake word. Positive dev and test sets have been manually cleaned to
discard any mispronunciations of the wake word (e.g. "Hi Snips" or "Hey
Snaips"), leaving the training set untouched.

The full dataset and its metadata are available for research
purposes as mentioned in the LICENSE file. Although some keyword spotting
datasets are freely available, such as the Speech Commands dataset for voice
 commands classification, there is no equivalent in the specific wake-word
 detection field. By establishing an open reference for wake-word detection,
  we hope to contribute to promote transparency and reproducibility in a
  highly concurrent field where datasets are often kept private.


## License summary

Use only for academic and/or research purposes. No commercial use.
Publication permitted only if the Data Sets are unmodified and subject to the same license terms.
Any publication must include a full citation to the paper in which the Data
Sets were initially published by Snips:

```
Coucke et al., 2018, "Efficient keyword spotting using dilated convolutions
and gating
```

Please read the full License Terms before accessing the Data Sets.

## Data Set access

To access the data, please write an email mentioning your affiliation and
the Data Set version to

```
research-datasets@snips.ai
```

You will be granted access shortly.
