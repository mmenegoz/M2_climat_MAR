# M2_climat_MAR
Computing climate trends over the Alps with MAR forced by ERA-20C

1. General description:

Downloading MAR data to investigate climate trends over the Alps.
For this we will use several classic Python packages:

    xarray: is an open-source project and Python package that makes working with labelled multi-dimensional arrays simple, efficient, and fun! (Xarray Tutorial / Xarray | SciPy 2020)
    jupyter: for using jupyter-notebook / lab
    matplotlib: back-end for making plots
    cartopy: replace basemap, back-end for map projections
    proplot: a lightweight matplotlib wrapper for making beautiful, publication-quality graphics (still in development)
    xesmf: Universal Regridder for Geospatial Data (only for Linux and Mac, an alternative is the interp function from xarray)

Check the Environment section at the end of this README if you want to know more about the environment and/or to install it on your local machine.

3. Environment

Note that we will be working with an already pre-installed environment with binder. If you want to install the same environment on your machine, you can do it directly by typing the command conda env create -f environment.yml using the environment file environment.yml from this repository (only functional under Linux, otherwise you can remove the xesmf package from the file for Windows). You need to have Anaconda or Minconda already pre-installed on your machine. If not, for Linux users, you can check this (steps 2, 3, and 4; the rest is to install it on a server — to adapt for non-Linux machines): https://mickaellalande.github.io/post/tutorial/how-to-install-jupyter-notebook-on-a-server/. For managing your conda environments always come back to the official documentation: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file.

The package versions can be found in the environment.yml file. Be careful if you want to upgrade this environment, because there are often conflicts between some packages (e.g., version 0.6.4 of proplot does not work with version 3.3 of matplotlib, or cartopy does not work with the latest version 3.9 of python... but this can have already evolved at the time of this session). Be particularly careful with Proplot which is a package under development and which evolves very quickly, including changes of syntax, thus refer to version 0.6.4 for these practical works: https://proplot.readthedocs.io/en/v0.6.4/.

Some issues related with this environment:

    xESFM installation: https://github.com/JiaweiZhuang/xESMF/issues/47
    xESFM NaN's: https://github.com/JiaweiZhuang/xESMF/issues/15
    Proplot colormaps: https://github.com/lukelbd/proplot/issues/123
    Proplot colorbar: https://github.com/lukelbd/proplot/issues/124
