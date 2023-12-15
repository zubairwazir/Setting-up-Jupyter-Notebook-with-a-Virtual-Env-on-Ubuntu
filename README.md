### **Step-by-Step Tutorial: Setting up Jupyter Notebook with a Virtual Environment on Ubuntu**

#### 1\. **Install Python 3 and venv**

Ensure Python 3 and venv are installed on your Ubuntu system. If not, install them using the package manager:

`sudo apt update sudo apt install python3 python3-venv`

#### 2\. **Create a Virtual Environment**

Open a terminal and create a virtual environment named **jupyter**:

`python3 -m venv jupyter`

#### 3\. **Activate the Virtual Environment**

Activate the virtual environment by running:

`source jupyter/bin/activate`

#### 4\. **Install Jupyter Notebook**

Ensure **pip** is updated and then install Jupyter Notebook:

`pip install jupyter`

#### 5\. **Create a Launcher Script**

Create a script that automatically activates the virtual environment and launches Jupyter Notebook.

Open a text editor and create a file named **jupyter-launcher.sh**. Paste the following content into the file:

`#!/bin/bash source /path/to/jupyter/bin/activate jupyter notebook "$@"`

Replace **/path/to/jupyter** with the absolute path to your virtual environment.

#### 6\. **Make the Script Executable**

Save the file and then make it executable:

`chmod +x jupyter-launcher.sh`

#### 7\. **Move the Script to a Directory in PATH**

Move the script to a directory included in the system's PATH to make it globally accessible:

`sudo mv jupyter-launcher.sh /usr/local/bin/jupyter`

#### 8\. **Run Jupyter Notebook**

You can now run Jupyter Notebook from anywhere by simply typing:

`jupyter`

This command activates the virtual environment and launches Jupyter Notebook.

#### 9\. **Install Some Basic Data Analysis Libraries**

Optionally, install data analysis libraries within the virtual environment:

`pip install pandas matplotlib seaborn numpy folium scipy scikit-learn statsmodels`

These steps guide you through setting up a virtual environment with Jupyter Notebook on Ubuntu and creating a launcher script to activate the environment and start Jupyter Notebook easily.
