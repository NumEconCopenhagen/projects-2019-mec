# Examproject

Our examproject consist of three parts:
  1) The dataproject
  2) The modelproject
  3) The examproject

**The dataproject** adresses the development of home care for people aged 65 years and above in Denmark. An API is used to fetch data from tables AED06, AED12 and BY2 from Statistics Denmark. 
Note that in order to fetch the data from Statistics Denmark we use the package `pydst`, which is not a default packages in python, and need to be install to be able to run the the notebook. In the last part of the notebook we have created a map of Denmark to make an easier comparion across municipalities. To create the map we use the package `geopandas`, which is not a defaul packages in python, and need to be install to be able to run the last piece of code in the notebook.
- *To install* `pydst` (works for both windows and mac)*: open terminal and run the command: pip install git+https://github.com/elben10/pydst*
- *To install* `geopandas`: 
    - *Windows: open terminal and run the command: conda install -c conda-forge geopandas*
    - *Mac: open terminal*
        1. Run the command: conda install -c conda-forge geopandas
        2. Uninstall fiona by running the command: conda uninstall fiona
        3. Download fiona wheel and install: can be downloaded from here (https://pypi.python.org/packages/71/ea/908bf078499b30d1ec374eb5baba016a568fc8142ee6ccf72e356d20871c/Fiona-1.7.4-cp27-cp27m-macosx_10_6_intel.whl#md5=971393c23ffc552664b7c694b992fb3e) and run: pip install Fiona-1.7.4-cp27-cp27m-macosx_10_6_intel.whl
        4. Reinstall geopandas by running the command: pip install git+git://github.com/geopandas/geopandas.git     
