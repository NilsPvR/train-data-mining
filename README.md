# Train data mining

This repo performs some data mining techniques on a train data set (literal train/🚄 not training) and explains the general idea of the used methods. This has been created for the practical exercise as part of my study in computer science for the module "Data Mining".

A Jupyter Notbook is used for the documentation and application of the techniques. To avoid cluttering of version control the output and metadata are stripped (see [Setup](#setup)). To document the results a full output will occasionally be commited to version control.

## The data

The data has been manually sampled during all my train rides starting in November 2023. The data set contains information about every train I took since the start of data collection. Due to resulting privacy concerns the original data set will not be published. However a small sample is provided to give a general idea of the data.
I initially started to document the train rides because I felt like the times I had a ticket inspection were dependent on the train line and time of day. The fact that I could use this data set for the module is a nice coincidence.

## Setup
To run this repo locally clone the repo.
```shell
git clone https://github.com/NilsPvR/train-data
```
Configure your [venv](https://docs.python.org/3/library/venv.html) and activate it.
```shell
python -m venv ./.venv
# activte depending on OS and Shell
```
Install required packages, e.g. with pip.
```shell
pip install -r requirements.txt
```
Configure the git filter for Jupyter Notebooks ([Credits](https://gist.github.com/33eyes/431e3d432f73371509d176d0dfb95b6e)).
```shell
# Change the filter according to your venv activation (docs link above)
git config filter.strip-notebook-output.clean 'source .venv/Scripts/activate && jupyter nbconvert --ClearOutputPreprocessor.enabled=True --to=notebook --stdin --stdout --log-level=ERROR'
```
