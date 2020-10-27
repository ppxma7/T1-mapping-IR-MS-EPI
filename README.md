# T1-mapping-IR-MS-EPI
T1 mapping code for the Inversion Recovery Multi-Shot Echo Planar Imaging sequence

This jupyter notebook enables the processing of data acquired using the sequence described in the paper (put doi here).

# MRI parameters
It requires a variety of imaging parameters such as number of TIs (nTIs), Multi-band factor (MBfactor), repetition time (TR) and slice offset (sliceOffsets) for the different TIs. The time between the inversion time and the first possible slice acquisition is also necessary (minTI). 

# Data format
The input data is nifti format, with all the different TIs inside a single nifti file (stored as different volumes), with both modulus and phase data necessary for the sign correction of the signal. Input directory (in_dir) and output directory (out_dir) need to be specified as well.

# Output data
The algorithm, after fitting T1 for each slice individually, output the T1, S0 and R2 (sum of squared difference between data and fit).
There is the possibility to also fit the data for imperfect inversion efficiency.
