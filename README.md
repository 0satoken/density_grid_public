## Density grids
This repo provides density grids generated from N-body simulation for field-level inference comparison project

* `download.sh`: Download script.
* `filelist.txt`: List of available data. Currently, matter density field (delta_*) and halo density field (halo_*) are available.
* `input_class_parameters.ini`: The parameter list of class used in initial condition generation. This file is generated from monofonic.
* `outputs.txt`: The scale factor when snapshots are dumped ($z = 4, 3, 2.5, 2, 1.5, 1, 0.5, 0.3, 0.1, 0$)
* `load_data.ipynb`: Sample Jupyter-Notebook to load the data.


### Technical details
The simulation is run with Gadget-4 ($L = 1.5 h^{-1} \, \mathrm{Gpc},\ N = 2048^3$)
and the initial condition ($z = 64$) is generated with monofonic at 3LPT assuming "Planck2018EE" cosmology.  
The density grids are computed with CIC assignment scheme and window function is deconvoluted in Fourier space.  
The halo finder is SubFind (on the fly in Gadget-4) and the halo mass definition is Mvir.--
There are 4 mass bins: [10^12.5, 10^13], [10^13, 10^13.5], [10^13.5, 10^14], [10^14, 10^14.5]
