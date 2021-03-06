# DIRECT NOISY SPEECH MODELING FOR NOISY-TO-NOISY VOICE CONVERSION

## Samples of Noisy-to-Noisy Voice Conversion Framework

Those samples come from the [paper](https://arxiv.org/abs/2111.07116).

Sampling Rate: 8000 Hz

Speech dataset: [VCC 2018 Evaluation set](https://datashare.ed.ac.uk/handle/10283/3061)

Noise dataset: [PNL 100 Nonspeech](http://web.cse.ohio-state.edu/pnl/corpus/HuNonspeech/HuCorpus.html) (N86 to N100 for evaluation set)

## Details of the Methods:
**Baseline**: VQ-VAE trained on the denoised speech data by DCCRN; **Noisy** means the converted speech was added with the separated background sounds.

**Upper Bound**: VQ-VAE trained on the clean speech data; **Noisy** means the converted speech was added with original background sounds.

**Proposed (Direct)**: noise-conditioning VQ-VAE trained on the denoised/noisy-paired speech data and separated background sounds; **Clean** means the converted speech was generated by the VQ-VAE using zero sequences as the noise-conditioning; **Noisy** means the noisy converted speech was directly generated by the VQ-VAE using separated background sounds as the noise-conditioning.

Due to the samples from Proposed (Indirect) and Proposed (Direct) have almost the same quality, only the latter is demonstrated here.

### 1. Noisy source (Speaker SF3;  Noise type: Cry (N93);  SNR: 15 dB):
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMDJf/noisy_sf3_30016_n93_snr15.wav"></audio>

Denosied source:
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQwOThf/denoised_sf3_30016_n93_snr15.wav"></audio>

Target (Speaker TF2): 
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQwODZf/TF2_30002.wav"></audio>

| Methods             | Clean         | Noisy            |
|---------------------|---------------|------------------|
|Baseline                    |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQwOTVf/base_clean_sf3tf2_30016_n93_snr15.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjIzODlf/da_15_sf3tf2_30016_n93.wav"></audio>   |
|Proposed (Direct))          |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQwOTZf/method2_clean_sf3tf2_30016_n93_snr15.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjI2MTZf/md_15_sf3tf2_30016_n93.wav"></audio>   |
|Upper Bound                 |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQwOTdf/upper_clean_sf3tf2_30016.wav"></audio>      |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjIyNzBf/ca_15_sf3tf2_30016_n93.wav"></audio>   |


### 2. Noisy source (Speaker SF4;  Noise type: Phone dialing (N100);  SNR: 7 dB):
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMTNf/noisy_sf4_30026_n100_snr7.wav"></audio>

Denosied source:
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMTFf/denoised_sf4_30026_n100_snr7.wav"></audio>

Target (Speaker TM2): 
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMDRf/TM2_30002.wav"></audio>

| Methods             | Clean         | Noisy            |
|---------------------|---------------|------------------|
|Baseline                    |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMDlf/base_sf4tm2_30026_n100_snr7.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjIzMjdf/da_7_sf4tm2_30026_n100.wav"></audio>   |
|Proposed (Direct)           |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMTBf/method2_sf4tm2_30026_n100_snr7.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjI1OTNf/md_7_sf4tm2_30026_n100.wav"></audio>   |
|Upper Bound                 |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxMTVf/upper_clean_sf4tm2_30026.wav"></audio>      |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjIyNDdf/ca_7_sf4tm2_30026_n100.wav"></audio>   |


### 3. Noisy source (Speaker SM3;  Noise type: Snore (N87);  SNR: 7 dB):
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTdf/noisy_sm3_30010_n87_snr7.wav"></audio>

Denosied source:
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTVf/denoised_sm3_30010_n87_snr7.wav"></audio>

Target (Speaker TF2): 
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNThf/TF2_30012.wav"></audio>

| Methods             | Clean         | Noisy            |
|---------------------|---------------|------------------|
|Baseline                    |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTBf/base_sm3tf2_30010_n87_snr7.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTJf/da_7_sm3tf2_30010_n87.wav"></audio>   |
|Proposed (Direct)           |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTZf/method2_sm3tf2_30010_n87_snr7.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTRf/md_7_sm3tf2_30010_n87.wav"></audio>   |
|Upper Bound                 |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTlf/upper_sm3tf2_30010.wav"></audio>      |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNTFf/ca_7_sm3tf2_30010_n87.wav"></audio>   |


### 4. Noisy source (Speaker SM4;  Noise type: Door moving (N98);  SNR: 7 dB):
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQ0MjBf/noisy_sm4_30023_n98_snr7.wav"></audio>

Denosied source:
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQzOTZf/denoised_sm4_30023_n98_snr7.wav"></audio>

Target (Speaker TM2): 
<audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQ0MjJf/TM2_30024.wav"></audio>

| Methods             | Clean         | Noisy            |
|---------------------|---------------|------------------|
|Baseline                    |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxNjFf/base_sm4tm2_30023_n98_snr7.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjIzNzlf/da_7_sm4tm2_30023_n98.wav"></audio>   |
|Proposed (Direct)           |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQxOTNf/method2_sm4tm2_30023_n98_snr7.wav"></audio>   |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjI2MTJf/md_7_sm4tm2_30023_n98.wav"></audio>   |
|Upper Bound                 |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMjA5NzQ0MjNf/upper_sm4tm2_30023.wav"></audio>      |   <audio id="audio" controls="" preload="none"><source id="wav" src="https://od.lk/s/NTBfMTk4NjIyNjZf/ca_7_sm4tm2_30023_n98.wav"></audio>   |
