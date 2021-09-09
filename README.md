# RadioML 2016
Fork of [adeeb10abbas/RadioML_2016](https://github.com/adeeb10abbas/RadioML_2016), which is a fork of [radioML/dataset](https://github.com/radioML/dataset) 
## Goal
Remove dependencies on gr-mapper and gr-mediatools

## Dependencies
* python
* gnuradio
* numpy
* scipy

## Setup
`conda create -n gnuradio`

`conda activate gnuradio`

`conda config --env --add channels conda-forge`

`conda config --env --set channel_priority strict`

`conda install numpy scipy gnuradio=3.8`

## Create Dataset
First, create an output folder

`mkdir datasets`

There are two constants in `generate_RML2016.10a.py`:
* `apply_channel` - whether or not to model the dynamic transmission channel
* `thermal_noise` - whether or not to model AWGN at the receiver
Set these parameters to your preference.

Then run:

`python generate_RML2016.10a.py`

## Changes
* We are using wavfile source instead of gr-mediatools.
* We are using built in modulations instead of gr-mapper
* Chnage analog source from serial podcast (which has a lot of silence) to public domain recording of The Star Spangled Banner (which was editted to remove silence at the beginning of the recording).
* Add option to turn off AWGN

