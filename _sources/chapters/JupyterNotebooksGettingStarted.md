# Jupyter Notebooks: Getting Started



## __<font color=blue>Option 1: Google Colab</font>__
---
Google Colab (short for Colaboratory) is a Jupyter notebook environment that __runs in your browser__ using Google Cloud. You do not have to download or install any software. Your notebooks are stored in your Google Drive and can be shared with others.

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabLogo.png
:alt: Google Colab Logo
:width: 100px
:align: center
```

- Go to [Google Colab](https://colab.research.google.com/). You can upload a Jupyter notebook from your PC by dragging and dropping it in the Upload window. _To create a new notebook, click “New notebook”._

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabUploadNew.png
:alt: Google Colab Uploading a Jupyter Notebook and Creating a New Notebook
:width: 600px
:align: center
```

- Data files (Excel or text) used in the Jupyter notebook need to be uploaded too! Go to your [Google Drive](https://drive.google.com/drive/my-drive) and find the directory in which the Jupyter notebook is stored (“My Drive – Colab Notebooks” by default). You can upload the data file from your PC by dragging and dropping it in the window.

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabDragDropData.png
:alt: Google Colab Uploading a Data File
:width: 600px
:align: center
```

- Loading files does require you to mount your Google Drive in your Colab notebook. First, open the file browser on the left-hand side. It will show a “Mount Drive” button. Once clicked, you will see a code cell appear. Run the code. You are taken to a Google authentication step. After accepting the conditions, copy the verification code and paste it in the area dedicated in your Colab notebook.

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabMountDrive.png
:alt: Google Colab Mounting Your Drive
:width: 600px
:align: center
```

- You can now interact with your Drive files in the file browser side panel. Click on the "three dots” icon next to a file to find _e.g_. the path information.

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabFilePath.png
:alt: Google Colab Finding File Path Information
:width: 600px
:align: center
```
 
- The following figure shows you how to insert, change type, edit, and run cells.
   - Recall that a Jupyter notebook consists of code cells that allow you to write and run programming code and text (=Markdown) cells that allow you to describe your workflow.
   - You can run any cell, code or text. Running a code cell will display the result or output below the code cell that you run. When you run a text cell, the text formatted using Markdown syntax will be rendered as stylized text.

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabMenu.png
:alt: Google Colab Menu Options
:width: 600px
:align: center
```
 
- Each Jupyter notebook uses a kernel. The kernel runs your code in a specific programming language, in our case, Python. It also maintains the state of your notebook’s computations. If your code is acting weird, sometimes it is best to clear all outputs and restart the kernel. This will clear all in memory objects and restart your code from the beginning of your notebook. The following figure shows you how.

```{image} ./Images-JupyterNotebooksGettingStarted/GoogleColabMenuKernel.png
:alt: Google Colab Kernel Options
:width: 600px
:align: center
```



## __<font color=blue>Option 2: Anaconda</font>__
---
Anaconda is an open-source Python and R distribution platform. It is __a package manager__ that helps you to work with multiple open-source packages and libraries by creating a reproducible environment.

```{image} ./Images-JupyterNotebooksGettingStarted/AnacondaLogo.png
:alt: Anaconda Logo
:width: 100px
:align: center
```
 
- Download [Anaconda](https://www.anaconda.com/download). We recommend downloading Anaconda’s latest Python version. It will take a while to download as it is a large file.

- Install the version of Anaconda which you downloaded, following the instructions.

- Launch the Jupyter notebook app by clicking on the Jupyter notebook icon installed by Anaconda in the start menu or by typing `jupyter notebook` in a terminal.

```{image} ./Images-JupyterNotebooksGettingStarted/JupyterNotebookLogo.png
:alt: Jupyter Notebook Logo
:width: 100px
:align: center
```

- A new browser window or tab will open showing the Jupyter notebook dashboard from which you can go to the directory in which you saved your Jupyter notebook on your PC. All Jupyter notebooks are identifiable by the notebook icon next to their name. Double click on the notebook you want to open. _To create a new notebook, click “New – Python 3”._

- If you include your data files (Excel or text) used in the Jupyter Notebook in the same directory, you do not need to include path information in your code.

```{image} ./Images-JupyterNotebooksGettingStarted/AnacondaJupyterNotebookOpenNew.png
:alt: Anaconda Jupyter Notebook Opening a Jupyter Notebook and Creating a New Notebook
:width: 600px
:align: center
```
 
- The following figure shows you how to insert, change type, edit, and run cells.
   - Recall that a Jupyter notebook consists of code cells that allow you to write and run programming code and text (=Markdown) cells that allow you to describe your workflow.
   - You can run any cell, code or text. Running a code cell will display the result or output below the code cell that you run. When you run a text cell, the text formatted using Markdown syntax will be rendered as stylized text.

```{image} ./Images-JupyterNotebooksGettingStarted/AnacondaJupyterNotebookMenu.png
:alt: Anaconda Jupyter Notebook Menu Options
:width: 600px
:align: center
```

- Each Jupyter notebook uses a kernel. The kernel runs your code in a specific programming language, in our case, Python. It also maintains the state of your notebook’s computations. If your code is acting weird, sometimes it is best to clear all outputs and restart the kernel. This will clear all in memory objects and restart your code from the beginning of your notebook. The following figure shows you how.
 
```{image} ./Images-JupyterNotebooksGettingStarted/AnacondaJupyterNotebookMenuKernel.png
:alt: Anaconda Jupyter Notebook Kernel Options
:width: 600px
:align: center
```



## __<font color=blue>Exercises</font>__
---

### __<font color=red>Data</font>__
---

- Get the data needed for these exercises [here](https://github.com/renee-85/PythonForBIOC0029/tree/master/data).

- Store the data somewhere you know, _e.g._ in a BIOC0029 folder in your Documents folder on your PC or in a BIOC0029 folder on your Google Drive.


### __<font color=red>Jupyter Notebooks</font>__
---

- Start a Jupyter Notebook file, either in Google Colab or Anaconda, to try out the exercises in the following chapters.

- Use the 'copy code to clipboard' symbol visible in the top right corner of code code cells when hovering over them to copy and paste code from the exercises to your Jupyter Notebook.

```{image} ./Images-JupyterNotebooksGettingStarted/CopyToClipboard.png
:alt: Copy code to clipboard symbol
:width: 600px
:align: center
```

- Use markdown cells and comment lines to explain the purpose of your Jupyter Notebook and code. 

- Execute code cells by placing your cursor in the code cell and hitting Shift and Enter. The result will print out in the Raw NBConverter output cell. 