# UK-SCAPE datalabs
DataLabs to access UK-SCAPE and hydrological agency monitoring data via [middleware](https://en.wikipedia.org/wiki/Middleware).

This GitHub repository is freely available to use, and without the DataLabs access. This repository can be cloned to your own local/remote workspace and you can test out the functionality for your own requirements. To be able to work on your own workspace, please make sure you have all the required python packages installed, they are listed at the top of each Notebook.

In this document we provide a step-by-step guide to:

i. [Overview and introduction to DataLabs](#overview_datalabs)

ii. [Importing the GitHub repository into DataLabs](#importing_repository)

iii. [Introduction to the repository notebooks](#introduction_notebooks)

<a id="overview_datalabs"></a>
### i. Overview and introduction to DataLabs
[DataLabs](https://datalab-docs.datalabs.ceh.ac.uk/index.html) is a NERC-funded, UKCEH-based, cloud-based, collaborative environment for developing data pipelines and analytical methods, that provides us with a secure area to collaborate with colleagues around the world. You can refer to this [video](https://www.youtube.com/watch?v=n68X8J4gj6Q) by Matt Fry, which has a brief introduction to DataLabs.

To use the DataLabs platform, you first need to get an account with DataLabs and also request access to the UKSCAPE Water project on DataLabs. After you have your username and password, please follow the steps given below to set up your very own DataLabs lab.

1. Go to the webpage https://datalab.datalabs.ceh.ac.uk/, and click on the "Log In" button.

2. Log in to the ceh-datalab-webpage with your created username and password. 

3. You will need to request access to the UKSCAPE Water Project and ukswater data store by emailing [Gemma Nash](mailto:gvp@ceh.ac.uk).

4. When you have been given access, click on "Open" tab for the UKSCAPE Water Project.

5. Click on "Notebooks" tab, in the left hand side panel under the "Analysis" section.

6. Click on the "Create Notebooks" tab, on the right side of the webpage. This will create a JupyterLab for you, which can host multiple notebooks.

7. Fill in the following information in the pop up, scroll down if required. 
  * *Display Name* - anything that you like
  * *Type* - select "JupyterLab" option
  * *URL Name* - any word (ideally similar to the Display Name without any space, dashes or underscore)
  * *Data Store* to Mount - select "ukswater" (you will need to have been granted permission)
  * *Description* - a few words describing the JupyterLab
  * *Sharing Status* - select "Private" option
  * *Assets* - leave empty or do not select any option

   Then click on the "Create" tab at the bottom. 
    
8. You should then see a new lab in your "Notebooks" page, with a blue "Requested" tab. Please wait, this should turn into a green "Ready" tab in a few minutes (you may need to refresh your browser window).

9. Click on the "Open" tab, associated with your newly created lab. 

10. This opens a new browser tab with your JupyterLab. Sometimes you may see a "Build Recommended" pop up. If it appears, click on the "Build" button. 

<a id="importing_repository"></a>
### ii. Importing the GitHub repository into DataLabs

11. Once you are in your JupyterLab in the new browser, scroll completely down in the "Launcher" section.

12. After you scroll down, you should see a "Terminal" tab in the "Other" section of the launcher. Double click on the "Terminal" tab.

13. This opens up a new "Terminal" in your launcher section with a command line prompt.

14. In the terminal, please type or copy and paste (using CTRL C + CTRL V) the following commands (followed by return/enter key). Exchange *NAME* in the first command with the jupterlab URL name you created in step 6. You can also find this *NAME* in your JupyterLab web browser address, i.e. the word before the "/lab". For example, if your *NAME* is new-project, the URL will be /data/notebooks/jupyterlab-new-project/.”
  * **cd /data/notebooks/jupyterlab-*NAME*/**
  * **ls**
  * **git clone --recursive https://github.com/NERC-CEH/uk-scape-datalabs.git**
  * **ls**
    If the all the commands are successful, the result of the last command should show a "uk-scape-datalabs" directory below the command prompt.

15. The previous step imports the UK-SCAPE data-labs GitHub repository to your DataLabs JupyterLab. You will also see a "uk-scape-datalabs" directory apprear in the File Browser panel on the left of your screen. After the "uk-scape-datalabs" directory shows up in your File Browser panel, go ahead and close the "Terminal 1" by clicking on the cross button next to it.

16. If you double-click on the "uk-scape-datalabs" directory in the File Browser panel, you will see the "python" directory and a "README.md" file, which is this file that you are currently reading. Click on the "python" directory to browse the repository notebooks.

<a id="introduction_notebooks"></a>
### iii. Introduction to the repository notebooks
Three python Jupyter notebooks are available:
- **Time series data access (Time-series-data-access.ipynb)**; this notebook provides examples of how to access hydrological monitoring agency data in a common format via node middleware from https://eip.ceh.ac.uk/hydrology-ukscape/. You can use this to display maps of station locations and timeseries graphs of individual stations for data from the EA, Met Office, NRFA, and SEPA.

- **Environment Agency (EA) water quality (WQ) data access (water-quality-data-access.ipynb)**; this notebook provides an example of how to retrieve EA WQ sites in a radius around a latitude/longitude point. The results are displayed on a map, and you can then see which determinands are measured at a particular site and plot a timeseries graph of a chosen determinand. 

- **Environment Agency (EA) water quality (WQ) data availability (EA WQ data availability.ipynb)**; this notebook provides access to pre-processed files that are regularly updated and have summary metadata about EA WQ sites, such as mean values and number of samples. The availability of determinands at locations can be determined, plotted to maps to compare different time periods, and a particular site's timeseries can be plotted for a chosen determinand for example.