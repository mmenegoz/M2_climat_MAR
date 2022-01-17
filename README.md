# M2_climat_MAR
Computing climate trends over the Alps with MAR forced by ERA-20C

This folder contain the french course from Martin Ménégoz, about climate modelling activities over mountainous areas.

The students are invited to read the two open-acess articles based on MAR experiments:

Beaumet, J., Ménégoz, M., Gallée, H., Fettweis, X., Morin, S., Six, D., Vincent, C., Wilhelm, B. and Anquetin, S., Twentieth century temperature and snow cover changes in the French Alps using a high-resolution regional climate model and reanalyses, Reg Environ Change 21, 114 (2021), https://doi.org/10.1007/s10113-021-01830-x

Ménégoz, M., Valla, E., Jourdain, N. C., Blanchet, J., Beaumet, J., Wilhelm, B., Gallée, H., Fettweis, X., Morin, S., and Anquetin, S., 2020: Contrasting seasonal changes in total and intense precipitation in the European Alps from 1903 to 2010, Hydrol. Earth Syst. Sci., 24, 5355–5377, https://doi.org/10.5194/hess-24-5355-2020

The students can use this binder session to create a python notebook to compute seasonal trends of temperature and precipitation over the Alps, using the MAR data available at:

**Temperature data: https://filesender.renater.fr/?s=download&token=a6240b77-15ba-45e2-8f16-98f4b1045069** (January 2022)
Precipitation and snow cover data could be shared also on this repository.

A zenodo repository with a more complete set of variables is also available there: https://zenodo.org/record/3674607#.YeNknmAo_OR

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mmenegoz/M2_climat_MAR/HEAD)

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

2. Script

MAR_alpine_climate_trends.ipynb is a basic script from which you can start working on the MAR data. You can use it ot or not depending on your skill in python. Fell free to use any other of your favorite software!

The package https://zenodo.org/record/4458780#.YeSjVGAo_OQ could be used to compute the statistical significance of the trends with the Mann Kendall criteria with more efficiency.

3. Environment

Note that we will be working with an already pre-installed environment with binder. If you want to install the same environment on your machine, you can do it directly by typing the command conda env create -f environment.yml using the environment file environment.yml from this repository (only functional under Linux, otherwise you can remove the xesmf package from the file for Windows). You need to have Anaconda or Minconda already pre-installed on your machine. If not, for Linux users, you can check this (steps 2, 3, and 4; the rest is to install it on a server — to adapt for non-Linux machines): https://mickaellalande.github.io/post/tutorial/how-to-install-jupyter-notebook-on-a-server/. For managing your conda environments always come back to the official documentation: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file.

The package versions can be found in the environment.yml file. Be careful if you want to upgrade this environment, because there are often conflicts between some packages (e.g., version 0.6.4 of proplot does not work with version 3.3 of matplotlib, or cartopy does not work with the latest version 3.9 of python... but this can have already evolved at the time of this session). Be particularly careful with Proplot which is a package under development and which evolves very quickly, including changes of syntax, thus refer to version 0.6.4 for these practical works: https://proplot.readthedocs.io/en/v0.6.4/.

Some issues related with this environment:

    xESFM installation: https://github.com/JiaweiZhuang/xESMF/issues/47
    xESFM NaN's: https://github.com/JiaweiZhuang/xESMF/issues/15
    Proplot colormaps: https://github.com/lukelbd/proplot/issues/123
    Proplot colorbar: https://github.com/lukelbd/proplot/issues/124
