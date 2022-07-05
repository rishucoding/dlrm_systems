* Use the package-list.txt file. 
* Remove the following packages from it: 
  - torch==1.10.1+cu111=pypi_0
  - pyqtwebengine==5.12.1=pypi_0
  - pyqtchart==5.12=pypi_0
  - protobuf==3.20.1=pypi_0
  - pyqt5-sip==4.19.18=pypi_0
  - torchvision==0.11.2+cu111=pypi_0
  - torchaudio==0.10.1+rocm4.1=pypi_0
* Create a cuda environment and use the package file: $ conda create -n harv --file package-list.txt -c conda-forge
* Install PyTorch using: conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cudatoolkit=11.3 -c pytorch -c conda-forge
* This installs the PyTorch which supports caffe2 and GPU. 
* To test: $ python dlrm_s_caffe2.py --inference_only --num_batches 512  --caffe2_net_type async_dag --config_file "configs/dlrm_rm1.json" --enable_profiling --engine "prof_dag" --nepochs 32
