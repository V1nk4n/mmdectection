# mmdectection
.venv

https://pytorch.org/get-started/locally/#start-locally: 
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

https://mmcv.readthedocs.io/en/2.x/get_started/installation.html: 
pip install -U openmim
mim install "mmcv>=2.0.0rc1"
mim install mmengine
mim install mmdet
ModuleNotFoundError: No module named 'mmcv._ext'

pip install mmcv==2.0.1 -f https://download.openmmlab.com/mmcv/dist/cu117/torch2.0/index.html
ImportError: DLL load failed while importing _ext: The specified procedure could not be found.

pip install mmcv>=2.0.0rc1 -f https://download.openmmlab.com/mmcv/dist/cu118/torch2.0/index.html
ImportError: DLL load failed while importing _ext: The specified procedure could not be found.

Try installing mmcv with MCV_WITH_OPS=1, FORCE_CUDA=1 and install mmcv from source
pip install mmcv-full -f https://download.openmmlab.com/mmcv/dist/cu117/torch1.13.1/index.html --no-cache-dir --force-reinstall
MMCV==1.7.2 is used but incompatible. Please install mmcv>=2.0.0rc4, <2.2.0. => mmcv-full latest version is 1.7.2 => CANT USE mmcv-full

#NOT YET TESTED
https://mmdetection.readthedocs.io/en/v2.2.0/install.html:
conda create -n open-mmlab python=3.7 -y
conda activate open-mmlab
# install latest pytorch prebuilt with the default prebuilt CUDA version (usually the latest)
conda install -c pytorch pytorch torchvision -y
git clone https://github.com/open-mmlab/mmdetection.git
cd mmdetection
pip install -r requirements/build.txt
pip install "git+https://github.com/open-mmlab/cocoapi.git#subdirectory=pycocotools"
pip install -v -e .
