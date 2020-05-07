# How to reproduce the following project on your system:

# Word Embeddings for Historical Text

### Author: William Hamilton (wleif@stanford.edu)
### [Project Website](http://nlp.stanford.edu/projects/histwords)

The Colab notebook written (Importing_Embeddings.ipynb), simply executes the 'example.sh' file provided in the HistWords repository, to download the pre-trained word emebddings for the english fiction corpora taken across all the time periods considered, by the original authors in their study. It also runs the 'example.py' file provided, as well as a custom file of your choice. ('nish.py' is the custom file I created on my system, as given in the notebook)

To implement this Colab notebook, kindly take note that the HistWords code should be run using Python 2.7. If you have opened a notebook in Google Colab, you will either need to connect to a hosted runtime, or a local runtime. (Check in the toolbar above)

If you are connected to a hosted runtime, you are using Google Cloud to run your code. Go to the options at the top of the webpage, and select 'Runtime'. Following this, select 'Python 2', to open a Python 2-run notebook.

If the 'Python 2' option is not found however, the other option would be to install Python 2 on your local machine, and connect your notebook to a local runtime instead. To do this, the following link will be found useful:  

https://research.google.com/colaboratory/local-runtimes.html

After successfully connecting your Colab notebook to a local runtime, you can now run it using Python 2.7, assuming it has been installed on your system. Your local directories will be visible on your left pane, if this is successful.

Following this, execute the following commands:

```
!git clone https://github.com/williamleif/histwords.git
```
This clones the HistWords repository onto your system, and these files can be accessed on your Colab notebook, using the sidebar visible on your left.
Note that when running this notebook again later on, there is no need to run this command again, as the repository will already be on your local machine.


You can use the `%pwd` and the `%cd` commands to print your working directory and change directories respectively, so that you are in the directory where the HistWords repository is present on your system.

```
!git clone https://github.com/scikit-learn/scikit-learn.git
```
This command can be used to clone the scikit-learn repository onto your system, as the sklearn library is needed to run the example provided. (No need to run this more than once, if you are using this notebook again)

```
!example.sh
```
This can be run, to download the pre-trained english fiction word vectors across all time periods, from the project website. (http://nlp.stanford.edu/projects/histwords)
You may edit this shell file, to download a different set of word vectors. Again, there is no need to run the shell file multiple times, if you are downloading the same set of embeddings, as they will already be on your system.


```
!python example.py
```
Running this will show how the vector representations are used, assuming `example.sh` has been run. This .py file can be edited to show the similarity between any two words, across different time periods.

# Note, when editing to run custom examples:

If you are unable to edit the .sh and .py files from Colab, simply make a local copy of the files on your machine, and edit them accordingly. Finally, upload them onto Colab, using the options in the left pane. Following this, they can be executed on Colab.
