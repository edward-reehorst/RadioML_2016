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
`conda create -n gnuradio python numpy scipy`
`conda activate gnuradio`
`conda install gnuradio -c conda-forge`

## Changes
* We are using wavfile source instead of gr-mediatools.
* We are using built in modulations instead of gr-mapper
* Chnage analog source from serial podcast (which has a lot of silence) to public domain recording of The Star Spangled Banner (which was editted to remove silence at the beginning of the recording).
* Add option to turn off AWGN

