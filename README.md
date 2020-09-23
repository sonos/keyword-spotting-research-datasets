# keyword-spotting-research-datasets

## Overview

### Reference

This repository contains the license and instructions relative to the open
Datasets mentioned in [this publication](https://arxiv.org/abs/1811.07684):

```
Coucke A. et al., "Efficient keyword spotting using dilated convolutions and gating",
```
accepted for publication to ICASSP 2019.

Any publication must include a full citation to this paper.

A different version was used in [Leroy D. et al., "Federated learning for keyword spotting"](https://arxiv.org/abs/1810.05512), also accepted for publication to ICASSP 2019. Please mention which version you want access to in the contact form (see below).

### Datasets

The wake word is "Hey Snips" pronounced with no pause between the two words. Both Data Sets contains a large variety of 
English accents and recording environments. Note that negative samples have been recorded in the same conditions than wake-word utterances, therefore arising from the same domain (speaker, hardware, environment, etc.).

The full datasets and their metadata are available for research purposes as mentioned in the LICENSE file. Although some 
keyword spotting datasets are freely available, such as the Speech Commands dataset for voice commands classification, 
there is no equivalent in the specific wake-word detection field. By establishing an open reference for wake-word 
detection, we hope to contribute to promote transparency and reproducibility in a highly concurrent field where datasets
 are often kept private.
 
The datasets are available upon requests as described in the Dataset access
section below.

Please note that the statistics displayed below might not
remain consistent with the datasets provided. Indeed, under the
GDPR and since voice recordings constitute personal data, dataset contributors
have the right to opt out, see [the full License Terms](https://github.com/snipsco/keyword-spotting-research-datasets/blob/master/LICENSE) for
more details.


#### Dataset 1: Coucke et al., 2019, "Efficient keyword spotting using dilated convolutions and gating"

Positive data has been cleaned by automatically removing samples of extreme duration (1st and 99th percentiles), or 
samples with repeated occurrences of the wake word. Positive dev and test sets have been manually cleaned to discard any
 mispronunciations of the wake word (e.g. "Hi Snips" or "Hey Snaips"), leaving the training set untouched.
 Around 11K wake word utterances and 86.5K negative examples have been recorded. 

|          |               |  Train |  Dev   |  Test  | 
|----------|---------------|--------|--------|--------| 
| Positive  | Utterances    | 5,876  | 2,504  | 25,88  | 
|          | Speakers      | 1,179  | 516    | 520    | 
|          | max / speaker | 10     | 10     | 10     | 
| Negative | Utterances    | 45,344 | 20,321 | 20,821 | 
|          | Speakers      | 3,330  | 1,474  | 1,469  | 
|          | max / speaker | 30     | 30     | 30     | 



#### Dataset 2: Leroy et al., 2019, "Federated learning for keyword spotting"

This crowdsourcing-induced data distribution mimicks a real-world non-i.i.d, unbalanced and highly distributed setting, and a parallel is drawn in the following work between a crowdsourcing contributor and a voice assistant user. The train, dev and test splits are built purposely using distinct users, 77\% of users being used solely for training while the 23\% remaining are used for parameter tuning and final evaluation. The dataset statistics are provided below

|            |  Train |  Dev  |  Test  |  Total | 
|------------|--------|-------|--------|--------| 
| Utterances | 53,991 | 8,337 | 7,854  | 69,582 | 
| Speakers   | 1,374  | 200   | 200    | 1,774  | 


#### Format

The dataset archive contains the following files:
```
* train.json
* dev.json
* test.json
* audio_files
  * uuid-id-1.wav
  * uuid-id-2.wav
  * uuid-id-3.wav
  * uuid-id-4.wav
  * ...
```

The `train`, `dev` and `test` files contain the list of audios for each part of the split, along with metadata. Each 
entry in those lists has the following attributes:

* `id`: a unique identifier for the entry
* `is_hotword`: `1` if the audio is a "Hey Snips" utterance, `0` otherwise
* `worker_id`: the unique identifier of the contributor - note that worker ids are not consistent across datasets 1 and 2 as they are re-generated for each one of them
* `duration`: the duration of the audio file in seconds
* `audio_file_path`: the relative path of the audio from the root of the directory eg `audio_files/<audio-uuid>`.

An example of such an entry is provided below:

```javascript
  {
    "id": "40084ea8-c576-4dba-a20b-fbda61f1de7d"
    "is_hotword": 1, 
    "worker_id": 12, 
    "duration": 1.86, 
    "audio_file_path": "audio_files/40084ea8-c576-4dba-a20b-fbda61f1de7d.wav", 
  }
```

## License summary

Use only for academic and/or research purposes. No commercial use.
Publication permitted only if the Datasets are unmodified and subject to the same license terms.
Any publication must include a full citation to the [paper](https://arxiv.org/abs/1811.07684) in which the
datasets were initially published by Snips<sup>1</sup>:

```
Coucke A. et al., 2019, "Efficient keyword spotting using dilated convolutions and gating,
```
accepted for publication to ICASSP 2019.

Please read [the full License Terms](https://github.com/sonos/keyword-spotting-research-datasets/blob/master/LICENSE) before accessing the Data Sets.

## Dataset access

To access the data, please fill the following form:

[https://forms.gle/JtmFYM7xK1SaMfZYA](https://forms.gle/JtmFYM7xK1SaMfZYA)

You will be granted access shortly and will be provided with a temporary url to download it.



<sup>1</sup> *The Snips team has joined Sonos in November 2019. These open datasets remain available and their access is now managed by the Sonos Voice Experience Team. Please email sve-research@sonos.com with any question.*
