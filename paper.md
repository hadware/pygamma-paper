---
title: 'PyGamma : a Python implementation of the Gamma inter-annotator agreement'
tags:
  - Python
  - linguistics
  - annotation
  - statistics
authors:
  - name: Rachid Riad
    orcid: 0000-0003-0872-7098 # todo, maybe
    affiliation: "1, 2"
  - name: Hadrien Titeux
    affiliation: 1
    # on met ACBL et Emmanuel?
affiliations:
 - name: LSCP/ENS/CNRS/EHESS/INRIA/PSL Research University, Paris, France 
   index: 1
 - name: NPI/ENS/INSERM/UPEC/PSL Research University, Cr ́eteil, France
   index: 2
   
date: 13 May 2020
bibliography: paper.bib
---

# Summary

A great part of the current efforts in Linguistic Studies and automated speech processing algorithms goes into recording audio corpora that are ever bigger in size and ever more diverse in origins. However, an audio corpus is close to useless for many applications if it hasn't been painstakingly annotated by human annotators to produce a reference anntation, that reliably indicates events contained in the audio track (be it speech [ami-corpus], baby noises [child-babble-corpus], animal vocalizations [birds-sounds-corpus], or even just plain noises). Moreover, indicating _when_ something happens in the audio is half of the work: in many cases, it's also important for the human annotator to indicate _what_ is the nature of the event. Indeed, many annotations are either categorical, or - in the case of speech - precise transcriptions [chat-childes-book] of the recorded speech. However, human annotators are suceptible to biases and errors, which raises the obvious question of the consistency and the reproducibility of their annotations. For these reasons, small parts of a corpora are usually annoted several times by different annotators, to assess the _agreement_ between annotators, and thus establish a numerical measure of that agreement. Consequently, the Gamma (γ) Inter-Annotator Agreement Measure was proposed by [chat-childes-book]. This measure (or metric) combines both of the common agreement paradigms : unitizing (_where_ are the annotations) and categorization (_what_ are the annotations).

The authors of [chat-childes-book] provided a Java freeware (and thus closed-source) implementation that cannot be used programatically (it's a GUI-based application). Moreover, its usage requires the user to register on the application's website. Additionaly, a lot of the work in either automated speech processing or linguistics today is done using Python [citation?]. For this reason, we thought it would greatly benefit both communities if we could provide them with a fully open-source Python implementation of the original algorithm.

The `PyGamma` package provides users with two ways to compute (in Python) the γ-agreement for a corpus. The first one is a simple one-call function that requires almost no understanding of the underlying framework. The second one is a object-oriented API that enables the user to build with more flexibility the right configuration of metrics used  to compute the γ-agreement and dissimilarity measures it is built upon.
It also features a command-line application that can be invoked directly from the shell, for those who prefer to use `bash` scripts for corpus processing.

We made sure that it is robustly tested using the widely-adopted `pytest` testing framework, and also back-tested it against the original Java implementation. Since some parts of the algorithm are fairly demanding, some parts of the computations are distributed using the `multiprocessing` standard Python API. We've used this software in our own custom-built annotation platform, Seshat [seshat].

< Who uses it, who will benefit from using it . Citation to Seshat as a first usage example>

# Mathematics

< mabe some explaining of what the lib does, copied from the Seshat paper > 


# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Fenced code blocks are rendered with syntax highlighting:
```python
for n in range(10):
    yield f(n)
```	

# How to cite us



# Acknowledgements

< Xuan Nga et alex pour les datasets? >
< le NPI et les financements? >

# References

