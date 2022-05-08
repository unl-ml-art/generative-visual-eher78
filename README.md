# Project 3 Generative Visual

Abraham Schaecher, aschaecher2@huskers.unl.edu
<!-- (Your teammate's contact info, if appropriate) -->

## Abstract

<!-- Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions. -->

For this project, I was interested in learning about the Seven Wonders of the Ancient World. Basically, these seven constructions are represented as some
of the earliest developments of the ancient world. All except for one structure (Great Pyramid of Giza) has been destroyed or lost in history by human
and environmental factors. The list of the remaining structures part of the Seven Wonders includes:
- Hanging Gardens of Babylon
- Statue of Zeus at Olympia
- Temple of Artemis at Ephesus
- Mausoleum at Halicarnassus
- Colossus of Rhodes
- Lighthouse of Alexandria

My goal or scope of this visual project is to attempt and recreate some of these constructions using a visual GAN and descriptions from primary sources
in an attempt to be as historically accurate as possible. Understandibly, there has been some recreations and reconstructions with some images but the 
purpose of this is determing what a GAN can be used to evaluate a historically significant construction given some documented context. 

Hence, it will be interesting to find out what a computer thinks or imagines what a historically significant structure was in time and what a human thinks
of the result of the recreated image.

## Model/Data

<!-- Briefly describe the files that are included with your repository:
- trained models
- training data (or link to training data) -->

There were two main models I used for this project. 
- CC12M Diffusion
- CLIP-Guided Diffusion

Both models involved the use of diffusion to create generated images but there are some differences. CC12M uses a dataset with 12 million image-text pairs for vision and text training. CLIP-Guided Diffusion meanwhile uses diffusion based on the CLIP text dataset to create images.

I specifically chose these two models as from previous experience, they are efficent in producing outputs that fitted the textual prompts. I also experimented with other GANs such as BigGAN, StyleGAN, and BigSleepGAN and those two diffusion models worked the best from initial testing.

I also have the prompts for each of the six constructions for the Seven Ancient Wonders of the World that I will use as an input for the diffusion models:
- **Hanging Gardens of Babylon:**
> An ancient stone building with multi-level terraces covered with exotic trees and plants 
- **Statue of Zeus at Olympia:**
> A marble temple with a statue of a man made out of ivory and gold with a scepter
- **Temple of Artemis at Ephesus:**
> An ancient greek temple made of white marble with various pillars and beautiful carvings
- **Mausoleum at Halicarnassus:**
> A tall ancient marble tomb monument with a stone staircase with a square base and pillars
- **Colossus of Rhodes:**
> A tall, ancient bronze statue on top of a marble pedestal overlooking a pier
- **Lighthouse of Alexandria:**
> A tall, ancient stone and limestone lighthouse overlooking an ancient harbor

## Code

<!--Your code for generating your project:
- Python: generative_code.py
- Jupyter notebooks: generative_code.ipynb -->
- [CC12M Model](https://colab.research.google.com/drive/1TBo4saFn1BCSfgXsmREFrUl3zSQFg6CC)
- [Clip Guided Diffusion Model](https://colab.research.google.com/drive/1V66mUeJbXrTuQITvJunvnWVn96FEbSI3)
- [Upscaled Images](https://colab.research.google.com/drive/1k2Zod6kSHEvraybHl50Lys0LerhyTMCo?usp=sharing)

(The CLIP Guided Diffusion Model is also linked in the files)
[CLIP Guided Diffusion Code](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/clipGuidedDiffusion.ipynb)

The upscale image code was used for the results to have a better resolution and image suitable for presentation and printing the results for the Spring 2022 Open Studios.

## Results

<!-- Documentation of your results in an appropriate format, both links to files and a brief description of their contents:
- image files (`.jpg`, `.png` or whatever else is appropriate)
- move files (uploaded to youtube or vimeo due to github file size limits)
- ... some other form -->
- **Hanging Gardens of Babylon:**
> An ancient stone building with multi-level terraces covered with exotic trees and plants 
![Babylon Result](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/sevenWondersResults/upscaleImages/babylon4_out.png)

- **Statue of Zeus at Olympia:**
> A marble temple with a statue of a man made out of ivory and gold with a scepter
![Zeus Result](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/sevenWondersResults/upscaleImages/zeus3_out.png)

- **Temple of Artemis at Ephesus:**
> An ancient greek temple made of white marble with various pillars and beautiful carvings
![Artemis Result](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/sevenWondersResults/upscaleImages/artemis1_out.png)

- **Mausoleum at Halicarnassus:**
> A tall ancient marble tomb monument with a stone staircase with a square base and pillars
![Mausoleum Result](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/sevenWondersResults/upscaleImages/mauseloeum1_out.png)

- **Colossus of Rhodes:**
> A tall, ancient bronze statue on top of a marble pedestal overlooking a pier
![Rhodes Result](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/sevenWondersResults/upscaleImages/rhodes3_out.png)

- **Lighthouse of Alexandria:**
> A tall, ancient stone and limestone lighthouse overlooking an ancient harbor
![Lighthouse Result](https://github.com/unl-ml-art/generative-visual-eher78/blob/master/sevenWondersResults/upscaleImages/lighthouse3_out.png)

Overall, I was satisfied with the results the diffusion models has generated for the images. I do believe if I was given more weeks in preparation, I could have refined the textual prompts and even experimented with other models to see the variety of images produced for replicating each ancient construction. I will say that this project gave me a glimpse into the potential of how generated reconstructions can accomplish given historical data and I really would like to revisit this project in the future for research and other experimentations on historical artifacts.

## Technical Notes

<!-- Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.) -->

I do believe all of the code is accomplishable by running on Colab. I will say that if you have access to a GPU (specifically the V100), the runtime for the Clip Guided Diffusion can decrease from 1.5 hours to 5 minutes. The other two models: CC12M and the upscaling images can take a short time to generate and access to an external GPU is not necessarly required.

## Reference

<!-- References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts -->

- [Clip Guided Diffusion](https://arxiv.org/abs/2110.02711)
- [Clip Guided Diffusion Repository](https://github.com/afiaka87/clip-guided-diffusion)
- [CC12M Paper](https://arxiv.org/abs/2102.08981)
- [CC12M Repository](https://github.com/google-research-datasets/conceptual-12m)
- [Seven Ancient Wonders of the Ancient World](https://en.wikipedia.org/wiki/Seven_Wonders_of_the_Ancient_World)
