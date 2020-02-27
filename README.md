# JupyterLab-DownloadUploadDisabled
This project contains the jupyter lab source code which has limited access like : Upload file is diasbled, Downloading file or notebook is disabled, Export notebook as is disabled in file menu


1. Download the source code from https://github.com/jupyterlab/jupyterlab. [you can download the dev_mode folder from my git hub page]
2. Download the source code in zip format from the page.
3. Extract the zip it will create a folder named "jupyterlab-master
4. Open terminal and browse to the folder and run below commands in sequence:
```
pip install node
export PUPPETEER_SKIP_CHROMIUM_DOWNLOAD=true
pip install --trusted-host=pypi.python.org --trusted-host pypi.org --trusted-host files.pythonhosted.org-e . -v
jlpm install --verbose
jlpm --verbose run build
```
5. This last command "jlpm --verbose run build" will build the jupyter-lab for dev mode in the folder jupyterlab-master/dev_mode
6. run jupyter in dev mode:

```
jupyter lab --dev-mode

```
7. If it will opens a page saying that ***Cannot find template: "index.html"***, Below error is for me:

**Cannot find template: "index.html"**
In "/Users/shrek/opt/anaconda3/lib/python3.7/site-packages/dev_mode/static"
  7.1 so after jlpm --verbose run build in folder jupyterlab-master a dev_mode folder gets generated copy the folder.
  7.2 paste this folder to the give error path 
  7.3 re run the command **jupyter lab --dev-mode**

8. What is change inside the code:
There was a requirement that the users of this jupyterlab should not able to use the Upload, Download, Export Notebook As,      Save Notebook etc functionality, This can be done by commenting certain line of code in .ts files which have the code for this functionaliy in the respective packages.

9. **Will soon Upload the files names and what to comment in order to disable some functionality in jupyter lab**
