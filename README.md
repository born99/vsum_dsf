# Video summarization based on Deep Semantic Features
The implementation is based on the paper "Video Summarization using Deep Semantic Features" in ACCV'16 [[arXiv](arxiv.org/abs/1609.08758)]


## Install dependency
The source is running on Python 2.7.
The environment can be installed via conda environment:

	$ conda create --name <env> --file <environment file>
	
For example:
	
	$ conda create --name video_summarization --file requirements.txt
	

This code utilizes tools provided by M. Gygli *et al.* [1].
You can set it up by:

	cd vsum_dsf
	git clone https://github.com/gyglim/gm_submodular.git
	cd gm_submodular
	python setup.py install --user

[1] Gygli, Grabner & Van Gool. Video Summarization by Learning Submodular Mixtures of Objectives. CVPR 2015.

\* The source are already set up with *gm_submodular*

### Download dataset and model parameters

The source can be tested on Summe dataset provided bt M. Gygli *et al.* [2].
To test the model in the paper, download a `data.zip` [**HERE**](https://www.dropbox.com/sh/lu4pmad4o59kvlj/AABZ_R412HJZnFvR_B_IEt00a?dl=0) and extract it in the folder `vsum_dsf`.

[2] Gygli M., Grabner, H., Riemenschneider, H., van Gool, L.: Creating summaries from user videos. ECCV 2014.

## Script

See the Demo.ipynb or run the script below to generate the video summaries:

	python script/summarize.py
	
For evaluation 
	python script/evaluate.py results/summe/smt_feat
