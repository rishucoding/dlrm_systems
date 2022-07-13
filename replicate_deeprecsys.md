* Create a cuda environment and use the package file: $ conda create -n harv --file package-list.txt -c conda-forge
* Install PyTorch using: $ conda install pytorch==1.10.1 torchvision==0.11.2 torchaudio==0.10.1 cudatoolkit=11.3 -c pytorch -c conda-forge
* $ pip install --upgrade protobuf
* This installs the PyTorch which supports caffe2 and GPU. 
* $ git clone https://github.com/harvard-acc/DeepRecSys
* $ cd models
* $ python dlrm_s_caffe2.py --inference_only --num_batches 512  --caffe2_net_type async_dag --config_file "configs/dlrm_rm1.json" --enable_profiling --engine "prof_dag" --nepochs 32
