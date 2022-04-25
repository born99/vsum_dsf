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

### Download dataset and model parameters

To test the model in the paper, download a `data.zip` [**HERE**](https://www.dropbox.com/s/zxp8dq18t0tqlk2/data.zip?dl=0) and extract it in the folder `vsum_dsf`.


## Example

See the [notebook](https://github.com/mayu-ot/vsum_dsf/blob/master/Demo.ipynb) or:

	python script/summarize.py
	python script/evaluate.py results/summe/smt_feat
