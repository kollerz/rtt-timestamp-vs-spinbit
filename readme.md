# RTT: Timestamps vs Spinbit

This repository contains an experiment that compares two different methods of measuring round trip time:

1. RTTs from TCP timestamps using the method described in \"[New Methods for Passive Estimation of TCP Round-Trip Times](http://cobweb.cs.uga.edu/~kangli/src/pam05.pdf)
2. RTTs from a square wave, as described in the [Proposal for adding a Spin Bit to QUIC](https://britram.github.io/draft-trammell-quic-spin/draft-trammell-quic-spin.html)

In particular, we want to find out whether the probabilistically adding a measurement header (e.g. timestamp) to some of the packets is able to achieve similar accuracy more efficiently than using a single bit.

To run, first [install python-libtrace](https://www.cs.auckland.ac.nz/~nevil/python-libtrace/). Then, install the required modules and start Jupyter:

```
pip install -r requirements.txt
jupyter notebook
```

Then, follow the instructions in the notebooks `00_extract_flows.ipynb` and `01_compare_rtts.ipynb`, respectively.