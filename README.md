RHD.py
======

Python wrapper for the RHD file format used by Intan-Tech products

Example Usage:

The following code snippit demonstrates how one would plot the data from an aplifier channel.

```python
import RHD
import matplotlib.pyplot as plt

myData = RHD.openRhd("/home/user/experement1/experement1.rhd")
myChannels = myData.channels
A0 = myChannels["A-000"]

plt.plot(A0.getTrace())
plt.show()
```

The RDH object also keeps track of the following data from the RHD file:

```
 actual_dsp_cutoff_frequency
 actual_impedance_test_frequency
 actual_lower_bandwidth
 actual_upper_bandwidth
 board_mode
 channels
 data_block_list
 desired_dsp_cutoff_frequency
 desired_impedance_test_frequency
 desired_lower_bandwidth
 desired_upper_bandwidth
 dsp_enabled
 header_identifier
 notch_cutoff_mode
 note
 number_of_signal_groups
 number_of_temperature_sensors
 sample_rate
 signal_groups
 version
```
