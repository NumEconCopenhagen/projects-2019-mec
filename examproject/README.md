# Overview of our portfolio

Our portfolio consists of three parts:
  1) A data project (in the folder /dataproject)
  2) A model project (in the folder /modelproject)
  3) An exam project (in the folder /examproject)
  4) A Feedback.txt file with a list of the groups each group member have given peer feedback to with links
     to the GitHub issues

**The data project** addresses the development of home care for people aged 65 years and above in Denmark. An API is used to fetch data from tables AED06, AED12 and BY2 from Statistics Denmark. 

*Dependencies:* In order to fetch the data from Statistics Denmark we use the package `pydst`, which is not a default package in Python, and need to be installed to be able to run the notebook. In the last part of the notebook, we have created a map of Denmark to make an easy comparison across municipalities. To create the map we use the package `geopandas`, which is not a default package in Python, and need to be installed to be able to run the last piece of code in the notebook. 
- To install `pydst` (works for both windows and mac)*: open terminal and run the command: pip install git+https://github.com/elben10/pydst*
- To install `geopandas`: 
    - Windows: open terminal and run the command: conda install -c conda-forge geopandas
    - Mac: open terminal
        1. Run the command: conda install -c conda-forge geopandas
        2. Uninstall fiona by running the command: conda uninstall fiona
        3. Download fiona wheel and install: can be downloaded from here (https://pypi.python.org/packages/71/ea/908bf078499b30d1ec374eb5baba016a568fc8142ee6ccf72e356d20871c/Fiona-1.7.4-cp27-cp27m-macosx_10_6_intel.whl#md5=971393c23ffc552664b7c694b992fb3e) and run: pip install Fiona-1.7.4-cp27-cp27m-macosx_10_6_intel.whl
        4. Reinstall geopandas by running the command: pip install git+git://github.com/geopandas/geopandas.git     

When the packages are installed the notebook should run without problems as long as the files: KOMMUNE.dbf, KOMMUNE.prj, KOMMUNE.shp and KOMMUNE.shx are saved the same place as the notebook (which they will be if our entire repository is downloaded together).

**The model project** presents and solves a standard two-good static labour supply model, where agents value leisure and consumption. The model is solved in three ways: theoretically, analytically and numerically. For the numerical optimisation, the chosen algorithm is a sequential (least-squares) quadratic programming (SQP) algorithm (SLSQP). Besides the simple model, we extend the model in two ways by including a proportional income tax and a progressive income tax. The size of the tax payment affects the income and therefore also hours worked and consumption level.

*Dependencies:* Apart from the standard packages in Anaconda Python 3 no additional packages or files are necessary to run the notebook.

**The examproject** answers the questions asked in the notebook provided for the exam. The structure of the project is equivalent to the structure of the notebook provided. 

*Dependencies:* The notebook should be able to run without problems. However, we have used the function `.root_scalar` in the `scipy` package to answer questions on the AS-AD model. If `.root_scalar`is not availaible it might be necessary to run `conda update scipy` in your terminal to be able to run the notebook. 

