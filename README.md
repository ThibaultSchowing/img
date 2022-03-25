# img
Public repository for public image access or other stuff

## GEPARD installation procedure


- Install [Anaconda](https://www.anaconda.com/products/individual) FOR THE USER ONLY (matter of path)
- (Untested on clean windows install) Install the mingw-w64 toolchain [here](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe/download). [Instructions](https://superuser.com/questions/1294343/install-gcc-in-git-for-windows-bash-environment)
- Download [GEPARD branch](https://gitlab.ipfdd.de/GEPARD/gepard/-/tree/Gepard+GepardEval) **zip** and extract.
- (Anaconda prompt) **cd Desktop/gepard-Gepard+GepardEval**
- (Anaconda prompt) Create conda env - **conda create --name "gepard-env" python=3.7**
- (Anaconda prompt)  **conda activate gepard-env**
- (Anaconda prompt) **pip install -r /path/to/requirements.txt**
- (Anaconda prompt) **conda install pytorch torchvision torchaudio cpuonly -c pytorch-lts**
- (Anaconda prompt) Install pywin32 using "**conda install pywin32**"  (the conda installation works better than the pip installation!)
- Check compiler
- The cython modules must be built with the two following commands **from the cythonModules directory**:
- (Anaconda prompt) **python setuptsp.py**
- (Anaconda prompt) **python setup_getMaxRect.py**
- (Git + Anaconda) Install the detectron2 framework, follow instructions from [here](https://github.com/facebookresearch/detectron2/blob/master/INSTALL.md)
- **options ** (Git or download and un compress zip) ** git clone https://github.com/facebookresearch/detectron2.git **
- (Anaconda prompt) **python -m pip install -e detectron2**
- python -m gepard

## To use GEPARD

- 1) open **Anaconda Prompt**
- 2) run **conda activate gepard-env**
- 3) Within the Anaconda prompt, move in the GEPARD directory on the Desktop. Run **cd Desktop/gepard-Gepard+GepardEval**. Use **dir** to list the content of the directory you are in. Use **cd ..** to move in the parent directory.
- 4) run **python -m gepard** or **python -m gepardevaluation** 

## Create batch shortcut

>set root=C:\Users\XXXX\anaconda3\
>call %root%\Scripts\activate.bat %root%
>call conda activate gepard-env
>call cd C:\Users\XXXX\Desktop\gepard-Gepard+GepardEval
>call python -m gepard

>pause

