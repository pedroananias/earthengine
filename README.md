# Google Earth Engine (GEE) API for Python: Introduction

Information on using the Google Earth Engine (GEE) platform through the Python language with examples explained in Jupyter notebooks. We emphasize that the examples presented in this document and in its notebooks were developed with a focus on aquatic environments, but can be adapted for any purpose.


# Anaconda (Jupyter Notebook)

Free suite that provides a series of tools dedicated to the areas of Machine Learning and Data Science, in addition to general use

- Download the tool from: https://www.anaconda.com/distribution

Why use it?

- Access to Python
- Access to development environments (Jupyther, Visual Studio Code, Spyder, Spyder, PyCharm, etc.)
- Access to hundreds of libraries/modules (over 1400), including: Numpy, Matplotlib, SciPy, Scikit-Learn, Pandas and TensorFlow


# Python environment setup

You must install the necessary development libraries. The following are suggested: (Note that the command nomenclature will be the same for installing any other package you want)

1. Google Earth Engine API - Multi-petabyte catalog of satellite imagery and geospatial datasets with planetary-scale analysis capabilities (https://earthengine.google.com): `python -m pip install earthengine-api`
2. Matplotlib - Creating graphs and general data visualizations (https://matplotlib.org): `python -m pip install matplotlib`
3. Pandas - Fast, powerful, flexible and easy to use open source data analysis and manipulation (https://pandas.pydata.org): `python -m pip install pandas`
4. Numpy - Supports arrays and multidimensional arrays, having a large collection of math functions to work with these structures (https://numpy.org) `python -m pip install numpy`
5. Requests - Making HTTP requests simpler and more human-friendly (https://requests.readthedocs.io/en/master): `python -m pip install requests`
6. Pillow - Adds support for opening and writing many different image formats (https://pillow.readthedocs.io): `python -m pip install pillow`
7. Scikit-learn - Open source machine learning (https://scikit-learn.org): `python -m pip install sklearn`
8. Scipy - Made for mathematicians, scientists and engineers (https://www.scipy.org): `python -m pip install scipy`
9. Natsort - Sort lists "naturally" (https://pypi.org/project/natsort): `python -m pip install natsort`
10. GeoJSON - Encoding and decoding data in GeoJSON format (https://pypi.org/project/geojson): `python -m pip install geojson`


# Multipack installation

It is possible to install all the above packages at once:

`python -m pip install earthengine-api matplotlib pandas numpy requests pillow sklearn scipy natsort geojson`

There are other libraries that are suggested throughout the development and will be dealt with in the presented algorithms, but they are part of the 'heart' of Python, therefore, they do not need to be installed.


# Python IDE

Below are listed some software/tools/IDEs available for Python development:

1. Jupyter Notebook - Practical and didactic! Tracks the Ananconda distribution (https://jupyter.org)
2. Microsoft Visual Studio Code - In my opinion, excellent! Free and with a wide variety of extensions (https://code.visualstudio.com)
3. PyCharm - Also really great with an excellent debugger! (https://www.jetbrains.com/pycharm)
4. Atom (https://atom.io/packages/ide-python)
5. Google Colab - A Jupyter Notebook in the cloud! *Requires account @unesp.br or @gmail.com (https://colab.research.google.com)

And so many others...one for every taste!


# Steps of this document and its files

We organize this document as follows, starting the connection with the GEE, to extracting an image and classifying it using machine learning/deep learning.

1. First connection to Google Earth Engine (GEE) API
2. Writing data to a log file with the 'logging' library
3. Keeping record of algorithm execution time with 'time' library
4. Collections, geometries and filters: extracting an image from GEE datasets at a given date and location
5. Spectral indices: applying NDVI to an image
6. Using water masks and cloud/cloud shadow
7. Extracting a PNG image from the GEE with Pillow
8. Transforming a GEE image into a Dataframe using Reduce Region, Numpy and Pandas
9. Applying a Random Forest classifier to an image and plotting the result with Matplotlib
10. Applying a Multi-layer Perceptron classifier to an image and plotting the result with Matplotlib
11. Saving sorted pixels in a geojson with the GeoJSON library
12. Saving a GEE image in GeoTIFF (band-separated)
