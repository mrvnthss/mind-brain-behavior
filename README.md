# Mind, Brain and Behavior <a href="https://github.com/mrvnthss/mind-brain-behavior"><img src="brain-icon.png" align="right" height="80"/></a>

This repository contains a collection of projects, essays, and reports that I produced while enrolled in the [Mind, Brain and Behavior](https://www.uni-giessen.de/de/studium/studienangebot/master/mbb) master's program at [Justus Liebig University Giessen](https://www.uni-giessen.de). Also included is the [LaTeX template](latex-template) that I used to write my essays and reports.

## Table of Contents

- [Programming Projects](#programming-projects)
    + [Deep Learning with Dobble](#deep-learning-with-dobble)
- [Psychophysics Experiments](#psychophysics-experiments)
    + [Visual Working Memory Capacity](#visual-working-memory-capacity)
    + [Brightness Discrimination (2AFC)](#brightness-discrimination-2afc)
- [Essays](#essays)
    + [Representation of Objects in Object Recognition](#representation-of-objects-in-object-recognition)
    + [A Postdictive Framework for Visual Awareness](#a-postdictive-framework-for-visual-awareness)
    + [Reaching and Grasping in Virtual Reality](#reaching-and-grasping-in-virtual-reality)
    + [Bridging Minds and Machines](#bridging-minds-and-machines)
- [Technical Reports](#technical-reports)
    + [Collecting, Processing, and Analyzing EEG Data](#collecting-processing-and-analyzing-eeg-data)
- [LaTeX Template](#latex-template)
- [Languages and Tools](#languages-and-tools)
- [References](#references)

## Programming Projects

### Deep Learning with Dobble

- **Module**: Computational Modeling (MBB-MA-AM-3)
- **Seminar**: Deep Learning (S2)

In order to gain practical experience in working with deep neural networks (DNNs), the *Deep Learning* seminar included an extensive hands-on project, which also counted towards the final grade for the course. Nina (a fellow student) and I built our project around the popular card game [*Dobble*](https://www.dobblegame.com). We implemented an algorithm that allowed us to generate custom *Dobble* decks, and we set up a deep learning pipeline to train, validate, and test arbitrary DNNs with the goal of teaching those networks to play the game. Specifically, as input images we passed two different *Dobble* playing cards on a colored background and asked the DNNs to return the unique emoji present on both playing cards. We then trained ResNet networks of different depths and compared their performance.

<div align="center">
    <img src="https://github.com/mrvnthss/deep-learning-with-dobble/blob/main/reports/figures/results/resnet-comparison.png?raw=true" alt="resnet-comparison" width="700">
    <p>Training results for ResNet networks of different depths.</p>
</div>

Finally, to familiarize ourselves with interpretability techniques, we visualized and analyzed intermediate activations of the trained ResNet-18 network at different layers.

The full project is hosted in the following repository: [deep-learning-with-dobble](https://github.com/mrvnthss/deep-learning-with-dobble).

## Psychophysics Experiments

### Visual Working Memory Capacity

- **Module**: Programming for Behavioral and Neurosciences (Elective)

Since I enjoy working on programming projects, I decided to take an additional programming course as one of the two required electives in the MBB program. The module *Programming for Behavioral and Neurosciences* focused on implementing experimental protocols in MATLAB (The MathWorks Inc., [2023](#matlab)) using the Psychtoolbox library (Brainard, [1997](#brainard-ptb); Kleiner et al., [2007](#kleiner-ptb); Pelli, [1997](#pelli-ptb)). We worked on several projects throughout the class, and each of us had to replicate a well-known experiment from scratch to serve as the final project for the class. I chose to implement an experiment by Vogel & Machizawa ([2004](#vogel-machizawa)) that can be used to test participants' visual working memory. Below is a dynamic preview of the experiment.

<div align="center">
    <img src="https://github.com/mrvnthss/visual-working-memory-capacity/blob/main/figures/experiment-demo.gif?raw=true" alt="visual-working-memory-capacity" width="600">
    <p>A dynamic illustration of my implementation of the experiment by Vogel & Machizawa (<a href="#vogel-machizawa">2004</a>).</p>
</div>

The technical report explaining my implementation of the experiment can be found here: [reports/programming-for-behavioral-and-neurosciences.pdf](reports/programming-for-behavioral-and-neurosciences.pdf)

The full project is hosted in the following repository: [visual-working-memory-capacity](https://github.com/mrvnthss/visual-working-memory-capacity).

### Brightness Discrimination (2AFC)

- **Module**: Programming for Behavioral and Neurosciences (Elective)

*and*

- **Module**: Computational Modeling (MBB-MA-AM-3)
- **Seminar**: Introduction to Computational Modeling (S1)

The first experiment we tackled in *Programming for Behavioral and Neurosciences* was a simple brightness discrimination task using the *method of constant stimuli* (2AFC paradigm). In this experiment, the implementation of a single trial is rather straightforward. Hence, the idea for this project was to familiarize ourselves with correctly implementing the logic of the 2AFC paradigm, while also getting the details such as accurate timing right. Below is a preview of the brightness discrimination task.

<div align="center">
    <img src="https://github.com/mrvnthss/brightness-discrimination-2afc/blob/main/figures/experiment-demo.gif?raw=true" alt="brightness-discrimination" width="600">
    <p>A dynamic illustration of the brightness discrimination task.</p>
</div>

In the *Introduction to Computational Modeling* seminar, we learned to apply different modeling approaches to data collected in experiments. Since I had already implemented my own experiment using a 2AFC paradigm, I decided to recycle the brightness discrimination experiment to serve as a starting point for the final project of the Computational Modeling seminar. Using the [psignifit](https://uni-tuebingen.de/en/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/neuronale-informationsverarbeitung/research/software/psignifit/) toolbox developed by Schütt et al. ([2016](#psignifit)), I wrote a MATLAB script that automatically generates a psychometric curve fitted to the data collected during the brightness discrimination task. Below is an example of such a psychometric curve.

<div align="center">
    <img src="https://github.com/mrvnthss/brightness-discrimination-2afc/blob/main/figures/sample-01.png?raw=true" alt="brightness-discrimination" width="600">
    <p>An example of a psychometric fit obtained using the <a href="https://uni-tuebingen.de/en/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/informatik/lehrstuehle/neuronale-informationsverarbeitung/research/software/psignifit/">psignifit</a> toolbox.
    <br>
    <em>Simulated data.</em></p>
</div>

The full project is hosted in the following repository: [brightness-discrimination-2afc](https://github.com/mrvnthss/brightness-discrimination-2afc).

## Essays

### Representation of Objects in Object Recognition

- **Module**: Visual Cognition and Object Perception (MBB-MA-THM-3)
- **Seminar**: Visual Object Perception (S1)

Shape-based object recognition theories propose that the visual system compares the two-dimensional image of a viewed object with representations stored in memory to recognize an object. Recognition is declared when a representation is found that closely matches the image projected onto the retina. While agreeing on this general approach, recognition theories based on shape differ significantly in how representations are stored in memory and how they are matched to the images of viewed objects. For example, these theories can be distinguished by their degree of view dependence and the dimensionality of the stored representations. In my essay, I review a study by Bülthoff & Edelman ([1992](#buelthoff-edelman)) that suggests that the visual system likely represents objects by multiple "two-dimensional snapshots" and uses an approximation scheme for recognition.

You can find the essay here: [essays/visual-object-perception.pdf](essays/visual-object-perception.pdf).

### A Postdictive Framework for Visual Awareness

- **Module**: Visual Cognition and Object Perception (MBB-MA-THM-3)
- **Seminar**: Visual Cognition (S2)

In this essay, I discuss the perceptual illusion known as the flash-lag effect. Essentially, when a stationary stimulus is briefly flashed in alignment with a moving stimulus, the flashed object is usually perceived to spatially lag the moving object. The following demo nicely illustrates this:

<div align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/60/Flash_lag.gif" alt="flash-lag effect" width="600">
    <p>Illustration of the flash-lag effect by <i>Laurent Perrinet</i>. <a href="https://creativecommons.org/licenses/by-sa/3.0">CC-BY-SA 3.0</a></p>
</div>

When the green square flashes, most observers report seeing the red square *in front* of the green square. What makes this phenomenon interesting is that, at the time of writing, there is no consensus among scientists about the underlying mechanisms. In my essay, I discuss a postdictive framework postulated by Eagleman & Sejnowski ([2000](#eagleman)), and I elaborate on the debate that the proposal of this framework sparked among researchers.

You can find the essay here: [essays/visual-cognition.pdf](essays/visual-cognition.pdf).

### Reaching and Grasping in Virtual Reality

- **Module**: Perception and Action (MBB-MA-THM-2)
- **Seminar**: Space Perception and Action (S1)

Virtual reality (VR) has rapidly evolved from a realm of entertainment to an invaluable research tool in a variety of disciplines. In this essay, I discuss the complexity of accurately translating real-world motor actions (e.g., reaching and grasping) into the virtual domain, and I focus in particular on the role that haptic feedback plays in this endeavor.

You can find the essay here: [essays/space-perception-and-action.pdf](essays/space-perception-and-action.pdf)

### Bridging Minds and Machines

- **Module**: Perception and Action (MBB-MA-THM-2)
- **Seminar**: Development of Perception and Action (S2)

State-of-the-art (SOTA) AI systems, especially deep neural networks, have achieved remarkable performance in diverse domains, from image classification and board games to language modeling and protein folding. For many tasks, the capabilities of SOTA systems have now surpassed those of humans. However, there is a significant gap between these systems and the nuanced intelligence exhibited by humans. In particular, many of these artificial systems adopt a supervised pattern recognition approach and lack a fundamental grasp of common sense and causal reasoning.

There is an emerging body of research that attempts to address these issues by drawing inspiration from developmental psychology. In particular, there are promising developments in network design that reflect an emerging understanding of physical principles (intuitive physics), and in unsupervised training schemes that attempt to mimic the predominantly exploratory learning characteristic of infancy. In my essay, I review two recent contributions to this area of research by Stetter and Lang ([2021](#stetter)) and Piloto et al. ([2022](#piloto)). The former have introduced a network that learns the dynamics of its environment in an unsupervised manner, mimicking the exploratory learning observed in human infants, while the latter have designed a network that is capable of learning intuitive physics from visual data alone by prioritizing object-level representations and exploiting the violation-of-expectation paradigm popular in developmental psychology.

You can find the essay here: [essays/development-of-perception-and-action.pdf](essays/development-of-perception-and-action.pdf)

## Technical Reports

### Collecting, Processing, and Analyzing EEG Data

- **Module**: Imaging and Recording Brain Activity (MBB-MA-AM-4)
- **Seminar**: Electroencephalography (S1)

The EEG seminar that's part of the [Mind, Brain and Behavior](https://www.uni-giessen.de/de/studium/studienangebot/master/mbb) program consists of theoretical sessions that focus on the theory behind EEG, as well as practical lab sessions that teach students how to conduct EEG experiments and how to collect, preprocess, and analyze EEG data. The report that you can find in this repository focuses on the latter aspects. Using the passive auditory oddball task as an example, I discuss the entire process of conducting an EEG experiment, including EEG preparation and data collection, data preprocessing, and data analysis.

Data preprocessing and analysis were performed in MATLAB (The MathWorks Inc., [2023](#matlab)) using common EEG toolboxes, such as EEGLAB (Delorme & Makeig, [2004](#eeglab)), ERPLAB (Lopez-Calderon & Luck, [2014](#erplab)), and others.

You can find the report here: [reports/eeg.pdf](reports/eeg.pdf).

## LaTeX Template

All of the essays and reports available in this repository have been typeset using a custom LaTeX template that I created along the way. You can find the full template, along with instructions on how to use it, [here](latex-template).

## Languages and Tools

<p align="left">
  <a href="https://jupyterlab.readthedocs.io/en/latest/" target="_blank" rel="noreferrer">
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="jupyter" width="40" height="40"/>
  </a>
  &nbsp;
  <a href="https://www.python.org" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/>
  </a>
  &nbsp;
  <a href="https://pytorch.org/" target="_blank" rel="noreferrer">
    <img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" alt="pytorch" width="40" height="40"/>
  </a>
  &nbsp;
  <a href="https://numpy.org" target="_blank" rel="noreferrer">
    <img src="https://github.com/numpy/numpy/blob/main/branding/logo/logomark/numpylogoicon.png?raw=true" alt="numpy" width="40" height="40"/>
  </a>
  &nbsp;
  <a href="https://opencv.org/" target="_blank" rel="noreferrer">
    <img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" alt="opencv" width="40" height="40"/>
  </a>
  &nbsp;
  <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/>
  </a>
  &nbsp;
  <a href="https://www.mathworks.com/" target="_blank" rel="noreferrer">
    <img src="https://upload.wikimedia.org/wikipedia/commons/2/21/Matlab_Logo.png" alt="matlab" width="40" height="40"/>
  </a>
  <a href="https://www.psychtoolbox.net" target="_blank" rel="noreferrer">
    <img src="https://www.psychtoolbox.net/wp-content/uploads/2022/03/no_background_purple_text.png" alt="pytorch" height="40"/>
  </a>
</p>

## References

- <a id='brainard-ptb'></a> Brainard, D. H. (1997). The Psychophysics toolbox. *Spatial Vision, 10*(4), 433–436. [https://doi.org/10.1163/156856897X00357](https://doi.org/10.1163/156856897X00357)

- <a id='buelthoff-edelman'></a> Bülthoff, H. H., & Edelman, S. (1992). Psychophysical support for a two-dimensional view interpolation theory of object recognition. *Proceedings of the National Academy of Sciences, 89*(1), 60–64. [https://doi.org/10.1073/pnas.89.1.60](https://doi.org/10.1073/pnas.89.1.60)

- <a id='eeglab'></a> Delorme, A., & Makeig, S. (2004). EEGLAB: An open source toolbox for analysis of single-trial EEG dynamics including independent component analysis. *Journal of Neuroscience Methods, 134*(1), 9–21. [https://doi.org/10.1016/j.jneumeth.2003.10.009](https://doi.org/10.1016/j.jneumeth.2003.10.009)

- <a id='eagleman'></a> Eagleman, D. M., & Sejnowski, T. J. (2000). Motion integration and postdiction in visual awareness. *Science, 287*(5460), 2036–2038. [https://doi.org/10.1126/science.287.5460.2036](https://doi.org/10.1126/science.287.5460.2036)

- <a id='kleiner-ptb'></a> Kleiner, M., Brainard, D. H., & Pelli, D. G. (2007). What’s new in Psychtoolbox-3? *Perception, 36*(ECVP Abstract Supplement), 14. [https://doi.org/10.1177/03010066070360S101](https://doi.org/10.1177/03010066070360S101)

- <a id='erplab'></a> Lopez-Calderon, J., & Luck, S. J. (2014). ERPLAB: An open-source toolbox for the analysis of event-related potentials. *Frontiers in Human Neuroscience, 8*. https://doi.org/10.3389/fnhum.2014.00213

- <a id='pelli-ptb'></a> Pelli, D. G. (1997). The VideoToolbox software for visual psychophysics: Transforming numbers into movies. *Spatial Vision, 10*(4), 437–442. [https://doi.org/10.1163/156856897X00366](https://doi.org/10.1163/156856897X00366)

- <a id='piloto'></a> Piloto, L. S., Weinstein, A., Battaglia, P., & Botvinick, M. (2022). Intuitive physics learning in a deep-learning model inspired by developmental psychology. *Nature Human Behaviour, 6*(9), 1257–1267. [https://doi.org/10.1038/s41562-022-01394-8](https://doi.org/10.1038/s41562-022-01394-8)

- <a id='psignifit'></a> Schütt, H. H., Harmeling, S., Macke, J. H., & Wichmann, F. A. (2016). Painfree and accurate Bayesian estimation of psychometric functions for (potentially) overdispersed data. *Vision Research, 122*, 105–123. [https://doi.org/10.1016/j.visres.2016.02.002](https://doi.org/10.1016/j.visres.2016.02.002)

- <a id='stetter'></a> Stetter, M., & Lang, E. W. (2021). Learning intuitive physics and one-shot imitation using state-action-prediction self-organizing maps. *Computational Intelligence and Neuroscience, 2021*(5590445). [https://doi.org/10.1155/2021/5590445](https://doi.org/10.1155/2021/5590445)

- <a id='matlab'></a> The MathWorks Inc. (2023). MATLAB (9.14.0) [Computer software]. The MathWorks Inc. [https://www.mathworks.com](https://www.mathworks.com)

- <a id='vogel-machizawa'></a> Vogel, E. K., & Machizawa, M. G. (2004). Neural activity predicts individual differences in visual working memory capacity. *Nature, 428*(6984), 748–751. [https://doi.org/10.1038/nature02447](https://doi.org/10.1038/nature02447)

## Acknowledgments

The icon included in the header of this README is designed by [Freepik](https://www.freepik.com/icon/brain_1829882).
