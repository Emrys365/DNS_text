## Description

This repository contains the transcripts of the speech data in the [Deep Noise Suppression (DNS) Challenge](https://github.com/microsoft/DNS-Challenge) test sets.

  * The transcripts are normalized to be lowercase and contain no punctuation (except for abbreviations such as `don't` and `one's`).

  * All numbers are written as words.

  * Each line contains an utterance ID, followed by the corresponding transcript.

Currently, the transcripts are available for the following test sets:

  * [DNS1](https://github.com/microsoft/DNS-Challenge/tree/interspeech2020/master) - Interspeech 2020
    * [tt_synthetic_no_reverb](https://github.com/Emrys365/DNS_text/tree/main/DNS1/tt_synthetic_no_reverb)
      * After [text normalization](https://huggingface.co/openai/whisper-large-v2#evaluation), WER of Whisper Large v2 on the clean speech (reference signal) is 4.4%.
    * [tt_synthetic_with_reverb](https://github.com/Emrys365/DNS_text/tree/main/DNS1/tt_synthetic_with_reverb)
      * After [text normalization](https://huggingface.co/openai/whisper-large-v2#evaluation), WER of Whisper Large v2 on the reverberant clean speech (reference signal) is 8.9%.

## Disclaimer

The transcripts are not guaranteed to be correct. They are obtained by the following procedure:

  1. Generate a transcript for each utterance using the [OpenAI-Whisper Large v2 model](https://huggingface.co/openai/whisper-large-v2).

  2. We listen to each speech sample and correct the transcript if necessary. The corrections include:

  * adding missed spoken words (usually at the beginning/end of the utterance)

  * correcting misheard words

  * removing unspoken words (also known as model hallucination)

  * removing incomplete words (usually at the beginning/end of the utterance)

## Contribution

We welcome any contribution to the transcripts. Please submit a pull request if

  * you find any errors in the transcripts.

  * you would like to contribute the transcripts for more DNS Challenge test sets.
