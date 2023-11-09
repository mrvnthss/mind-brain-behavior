# Mind, Brain and Behavior

This repository contains a collection of essays that I wrote as part of the master's program [Mind, Brain and Behavior (MSc)](https://www.uni-giessen.de/de/studium/studienangebot/master/mbb) at [Justus Liebig University Giessen](https://www.uni-giessen.de/jlyou/en/index.html). [Here](latex-template), you can also find the [LaTeX](https://www.latex-project.org) template that I used to typeset the essays.

## Table of Contents

- [Essays](#essays)
- [LaTeX Template](#latex-template)
- [References](#references)

## Essays

### EEG

The EEG seminar that's part of the [Mind, Brain and Behavior](https://www.uni-giessen.de/de/studium/studienangebot/master/mbb) program at JLU consists of theoretical sessions that focus on the theory behind EEG, as well as practical lab sessions that teach students how to conduct EEG experiments and how to collect, preprocess, and analyze EEG data. My paper, which you can find in this repository, focuses on the latter aspects. Using the passive auditory oddball task as an example, I discuss the entire process of running an EEG experiment, including EEG preparation and data collection, data preprocessing, and data analysis.

Data preprocessing and analysis were performed in MATLAB (The MathWorks Inc., [2023](#matlab)) using common EEG toolboxes, such as EEGLAB (Delorme & Makeig, [2004](#eeglab)), ERPLAB (Lopez-Calderon & Luck, [2014](#erplab)), and others.

### Programming for Behavioral and Neurosciences

This paper is a technical report describing the implementation of a [visual working memory capacity experiment](https://github.com/mrvnthss/visual-working-memory-capacity) by Vogel & Machizawa ([2004](#vogel-machizawa)). The experiment is implemented in MATLAB (The MathWorks Inc., [2023](#matlab)) using the Psychtoolbox library (Brainard, [1997](#brainard-ptb); Kleiner et al., [2007](#kleiner-ptb); Pelli, [1997](#pelli-ptb)).

The idea is to test participants' visual working memory capacity in the following way: At the beginning of each trial, an arrow is briefly flashed just above a central fixation cross, pointing either left or right. Next, two arrays of the same number of colored squares are briefly presented. After a retention interval of just under one second, the two arrays of colored squares are presented again. However, in half of the trials, one of the squares in the hemifield to which the arrow pointed changes color. At the end of each trial, participants have to indicate whether this was the case or not. 

<div align="center">
    <img src="https://github.com/mrvnthss/visual-working-memory-capacity/blob/main/figures/experiment-demo.gif?raw=true" alt="trial-structure" width="600">
    <p>A dynamic illustration of the experiment by Vogel & Machizawa (<a href="#vogel-machizawa">2004</a>).</p>
</div>

For more details, please check out [this repository](https://github.com/mrvnthss/visual-working-memory-capacity).

### Space Perception and Action

Virtual Reality (VR) has rapidly evolved from a realm of entertainment to an invaluable tool in research across a variety of disciplines. In this essay, I discuss the the complexity of accurately translating real-world motor actions (e.g., reaching and grasping) into the virtual domain, and I focus in particular on the role that haptic feedback plays in this endeavor.

### Visual Cognition

In this essay, I discuss the perceptual illusion known as the flash-lag effect. Essentially, when a stationary stimulus is briefly flashed in alignment with a moving stimulus, the flashed object is usually perceived to spatially lag the moving object. The following illustration nicely demonstrates this:

<div align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/60/Flash_lag.gif" alt="flash-lag effect" width="600">
    <p>Illustration of the flash-lag effect by <i>Laurent Perrinet</i>. <a href="https://creativecommons.org/licenses/by-sa/3.0">CC-BY-SA 3.0</a></p>
</div>

When the green square flashes, most observers report seeing the red square *in front* of the green square. What makes this phenomenon interesting is that, at the time of writing, no consensus had been reached among scientists about the underlying meachnisms.

In my essay, I discuss a postdictive framework postulated by Eagleman & Sejnowski ([2000](#eagleman)), and I elaborate on the debate that the proposal of this framework sparked among researchers.

### Visual Object Perception

Shape-based object recognition theories propose that the visual system compares the twodimensional image of a viewed object to representations stored in memory to recognise an object. Recognition is declared if a representation is found that closely matches the image projected onto the retina. While agreeing on this overall approach, recognition theories based on shape differ significantly regarding how representations are stored in memory and how these are matched to the images of viewed objects. For example, these theories can be differentiated by their degree of view-dependency and the dimensionality of the stored representations. In my essay, I review a study by Bülthoff & Edelman ([1992](#buelthoff-edelman)), which suggests that the visual system likely represents objects by multiple 'two-dimensional snapshots' and uses an approximation scheme for recognition.

## LaTeX Template

All of the essays available in this repository are based on a LaTeX template that I have created myself. I have uploaded the full template [here](latex-template) along with instructions on how to use this template, should you wish to do so.

## References

- <a id='brainard-ptb'></a> Brainard, D. H. (1997). The Psychophysics Toolbox. *Spatial vision, 10*(4), 433–436. [https://doi.org/10.1163/156856897X00357](https://doi.org/10.1163/156856897X00357)

- <a id='buelthoff-edelman'></a> Bülthoff, H. H., & Edelman, S. (1992). Psychophysical support for a two-dimensional view interpolation theory of object recognition. *Proceedings of the National Academy of Sciences, 89*(1), 60–64. [https://doi.org/10.1073/pnas.89.1.60](https://doi.org/10.1073/pnas.89.1.60)

- <a id='eeglab'></a> Delorme, A., & Makeig, S. (2004). EEGLAB: an open source toolbox for analysis of single-trial EEG dynamics including independent component analysis. *Journal of Neuroscience Methods, 134*(1), 9–21. [https://doi.org/10.1016/j.jneumeth.2003.10.009](https://doi.org/10.1016/j.jneumeth.2003.10.009)

- <a id='eagleman'></a> Eagleman, D. M., & Sejnowski, T. J. (2000). Motion Integration and Postdiction in Visual Awareness. *Science, 287*(5460), 2036–2038. [https://doi.org/10.1126/science.287.5460.2036](https://doi.org/10.1126/science.287.5460.2036)

- <a id='kleiner-ptb'></a> Kleiner, M., Brainard, D. H., & Pelli, D. G. (2007). What’s new in Psychtoolbox-3? *Perception, 36*(ECVP Abstract Supplement), 14. [https://doi.org/10.1177/03010066070360S101](https://doi.org/10.1177/03010066070360S101)

- <a id='erplab'></a> Lopez-Calderon, J., & Luck, S. J. (2014). ERPLAB: an open-source toolbox for the analysis of event-related potentials. *Frontiers in Human Neuroscience, 8*. https://doi.org/10.3389/fnhum.2014.00213

- <a id='pelli-ptb'></a> Pelli, D. G. (1997). The VideoToolbox software for visual psychophysics: transforming numbers into movies. *Spatial vision, 10*(4), 437–442. [https://doi.org/10.1163/156856897X00366](https://doi.org/10.1163/156856897X00366)

- <a id='matlab'></a> The MathWorks Inc. (2023). MATLAB (9.14.0) [Computer software]. The MathWorks Inc. [https://www.mathworks.com](https://www.mathworks.com)

- <a id='vogel-machizawa'></a> Vogel, E. K., & Machizawa, M. G. (2004). Neural activity predicts individual differences in visual working memory capacity. *Nature, 428*(6984), 748–751. [https://doi.org/10.1038/nature02447](https://doi.org/10.1038/nature02447)

[def]: #references
