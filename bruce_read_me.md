## Install

```
git clone https://github.com/OpenPerceptionX/PersFormer_3DLane.git
cd PersFormer_3DLane/

conda create -n lanemd_torch18 python=3.8 -y

conda activate lanemd_torch18

conda install pytorch==1.8.1 torchvision==0.9.1 torchaudio==0.8.1 cudatoolkit=10.2 -c pytorch


pip3 install -r requirements.txt

cd models/nms/
python setup.py install

cd ../ops/
bash make.sh
```


## Train

* 2D only (lane3d_1000), speed is about 2 itrs per second

```
```
python -m torch.distributed.launch --nproc_per_node 1  main_persformer.py --mod=bruce_2d_only --batch_size=2 --nepochs=100
```

* 2D only (lane3d_300)
```
python -m torch.distributed.launch --nproc_per_node 1  main_persformer.py --mod=bruce_2d_only --batch_size=2 --nepochs=100
```