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

## Code

<!--Your code for generating your project:
- Python: generative_code.py
- Jupyter notebooks: generative_code.ipynb -->
-[CC12M Code](https://colab.research.google.com/drive/1TBo4saFn1BCSfgXsmREFrUl3zSQFg6CC)
-[Clip Guided Diffusion](https://colab.research.google.com/drive/1V66mUeJbXrTuQITvJunvnWVn96FEbSI3)

## Results

Documentation of your results in an appropriate format, both links to files and a brief description of their contents:
- image files (`.jpg`, `.png` or whatever else is appropriate)
- move files (uploaded to youtube or vimeo due to github file size limits)
- ... some other form

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts
