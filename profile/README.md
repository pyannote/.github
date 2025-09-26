![Identify who speaks when with pyannote](banner.jpg)

## 💚 Simply detect, segment, label, and separate speakers in any language 

[🎈 `pyannoteAI` playground](https://dashboard.pyannote.ai/) // [📚 `pyannoteAI` documentation](https://docs.pyannote.ai/) // [🎹 `pyannote` open-source toolkit](https://github.com/pyannote/pyannote-audio) // [🤗 `pyannote` pretrained models](https://huggingface.co/pyannote) // ![Github stars](https://img.shields.io/github/stars/pyannote/pyannote-audio?color=g) ![PyPI Downloads](https://static.pepy.tech/personalized-badge/pyannote-audio?period=total&units=international_system&left_color=grey&right_color=brightgreen&left_text=downloads)


### 🎤 What is speaker diarization?

![Diarization](diarization.jpg)


**Speaker diarization** is the process of automatically partitioning the audio recording of a conversation into segments and labeling them by speaker, answering the question **"who spoke when?"**. As the **foundational layer of conversational AI**, speaker diarization provides high-level insights for human-human and human-machine conversations, and unlocks a wide range of downstream applications: meeting transcription, call center analytics, voice agents, video dubbing.

### 🏆 State-of-the-art models

[`pyannoteAI`](https://www.pyannote.ai/) research team trains cutting-edge speaker diarization models, thanks to [**Jean Zay**](http://www.idris.fr/eng/jean-zay/) 🇫🇷 supercomputer managed by [**GENCI**](https://www.genci.fr/) 💚. They come in two flavors:

* [`pyannote.audio`](https://github.com/pyannote/pyannote-audio) open models available on [Huggingface](https://hf.co/pyannote) and used by 140k+ developers over the world ;
* premium models available on [`pyannoteAI` cloud](https://dashboard.pyannote.ai) that provide state-of-the-art speaker diarization as well as additional enterprise features (confidence scores, voiceprinting, ...)

### ▶️ Getting started

Install [`pyannote.audio`](https://github.com/pyannote/pyannote-audio) latest release available from ![Latest release](https://img.shields.io/pypi/v/pyannote-audio?color=059669) with either `uv` (recommended) or `pip`:

```bash
$ uv add pyannote.audio
$ pip install pyannote.audio
```

Enjoy state-of-the-art speaker diarization:

```python
# download pretrained pipeline from Huggingface
from pyannote.audio import Pipeline
pipeline = Pipeline.from_pretrained('pyannote/speaker-diarization-community-1', token="HUGGINGFACE_TOKEN")

# perform speaker diarization locally
output = pipeline('/path/to/audio.wav')

# enjoy state-of-the-art speaker diarization
for turn, speaker in output.speaker_diarization:
    print(f"{speaker} speaks between t={turn.start}s and t={turn.end}s")
```

Read [`community-1` model card](https://hf.co/pyannote/speaker-diarization-community-1) to make the most of it.

### ⏩️ Going further, better, and faster

Create a [`pyannoteAI`](https://dashboard.pyannote.ai) account, change one line of code, and enjoy free cloud credits to try [`precision-2`](https://pyannote.ai/blog/precision-2) premium diarization:

```python
# perform premium speaker diarization on pyannoteAI cloud
pipeline = Pipeline.from_pretrained('pyannote/speaker-diarization-precision-2', token="PYANNOTEAI_API_KEY")
better_output = pipeline('/path/to/audio.wav')
```


### 🎉 Join the community

[Discord](https://discord.gg/4cjCJcZv) // [X](https://x.com/pyannoteAI) // [LinkedIn](https://www.linkedin.com/company/pyannoteai/) // [Huggingface](https://hf.co/pyannote) // [Github](https://github.com/pyannote)

