# Disco Diffusion

<a href="https://colab.research.google.com/github/alembics/disco-diffusion/blob/main/Disco_Diffusion.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/></a>

A frankensteinian amalgamation of notebooks, models and techniques for the generation of AI Art and Animations.

[to be updated with further info soon]




## Changelog
#### v1 Oct 29th 2021 - Somnai
      
* QoL improvements added by Somnai (@somnai_dreams), including user friendly UI, settings+prompt saving and improved google drive folder organization.

#### v1.1 Nov 13th 2021 - Somnai
* Now includes sizing options, intermediate saves and fixed image prompts and perlin inits. unexposed batch option since it doesn't work

#### v2 Update: Nov 22nd 2021 - Somnai

* Initial addition of Katherine Crowson's Secondary Model Method (https://colab.research.google.com/drive/1mpkrhOjoyzPeSWy2r7T8EYRaU7amYOOi#scrollTo=X5gODNAMEUCR)

* Noticed settings were saving with the wrong name so corrected it. Let me know if you preferred the old scheme.

#### v3 Update: Dec 24th 2021 - Somnai

* Implemented Dango's advanced cutout method

* Added SLIP models, thanks to NeuralDivergent

* Fixed issue with NaNs resulting in black images, with massive help and testing from @Softology

* Perlin now changes properly within batches (not sure where this perlin_regen code came from originally, but thank you)

#### v4 Update: Jan 2021 - Somnai

* Implemented Diffusion Zooming

* Added Chigozie keyframing

* Made a bunch of edits to processes

#### v4.1 Update: Jan 14th 2021 - Somnai

* Added video input mode

* Added license that somehow went missing

* Added improved prompt keyframing, fixed image_prompts and multiple prompts

* Improved UI

* Significant under the hood cleanup and improvement

* Refined defaults for each mode

* Added latent-diffusion SuperRes for sharpening

* Added resume run mode

#### v5 Update: Feb 20th 2022 - gandamu / Adam Letts

* Added 3D animation mode. Uses weighted combination of AdaBins and MiDaS depth estimation models. Uses pytorch3d for 3D transforms on Colab and/or Linux.


## Notebook Provenance 

Original notebook by Katherine Crowson (https://github.com/crowsonkb, https://twitter.com/RiversHaveWings). It uses either OpenAI's 256x256 unconditional ImageNet or Katherine Crowson's fine-tuned 512x512 diffusion model (https://github.com/openai/guided-diffusion), together with CLIP (https://github.com/openai/CLIP) to connect text prompts with images.

Modified by Daniel Russell (https://github.com/russelldc, https://twitter.com/danielrussruss) to include (hopefully) optimal params for quick generations in 15-100 timesteps rather than 1000, as well as more robust augmentations.

Further improvements from Dango233 and nsheppard helped improve the quality of diffusion in general, and especially so for shorter runs like this notebook aims to achieve.

Vark added code to load in multiple Clip models at once, which all prompts are evaluated against, which may greatly improve accuracy.

The latest zoom, pan, rotation, and keyframes features were taken from Chigozie Nri's VQGAN Zoom Notebook (https://github.com/chigozienri, https://twitter.com/chigozienri)

Advanced DangoCutn Cutout method is also from Dango223.

--

Somnai (https://twitter.com/Somnai_dreams) added 2D Diffusion animation techniques, QoL improvements and various implementations of tech and techniques, mostly listed in the changelog below.

3D animation implementation added by Adam Letts (https://twitter.com/gandamu_ml) in collaboration with Somnai.