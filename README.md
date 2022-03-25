# img
Public repository for public image access or other stuff

## GEPARD installation procedure


- Install [Anaconda](https://www.anaconda.com/products/individual)
- (Untested on clean windows install) Install the mingw-w64 toolchain [here](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe/download). [Instructions](https://superuser.com/questions/1294343/install-gcc-in-git-for-windows-bash-environment)
- Download [GEPARD branch](https://gitlab.ipfdd.de/GEPARD/gepard/-/tree/Gepard+GepardEval) **zip** and extract.
- (Anaconda prompt) **cd Desktop/gepard-Gepard+GepardEval**
- (Anaconda prompt) Create conda env - **conda create --name "gepard-deploy-test" python=3.7**
- (Anaconda prompt)  **conda activate gepard-deploy-test**
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

