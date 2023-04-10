<img src='https://www.albertpumarola.com/images/2021/D-NeRF/teaser2.gif'  width=1000>

## One Frame Of Video

<div align=center>
  
<img  src="https://user-images.githubusercontent.com/33378412/230987182-6845c67e-8088-437a-b8de-0320ffc0b1ed.png" width="320" height="33%">
<img  src="https://user-images.githubusercontent.com/33378412/230985756-454dabe0-5e16-4489-ad45-c791002b75dc.png" width="320" height="33%"> 
<img  src="https://user-images.githubusercontent.com/33378412/230985688-62b831ee-16b0-41d5-87f9-75de1ca90e49.png" width="320" height="33%">

 </div>
 
 ## Reconstruct Mesh
 
 <div align=center>
  
<img  src="https://user-images.githubusercontent.com/33378412/230987598-560c93b7-36a0-4f89-b00b-9761bd808647.png" width="320" height="33%">
<img  src="https://user-images.githubusercontent.com/33378412/230987616-3c74093c-ba4f-4adf-a15b-3cef8718c408.png" width="320" height="33%"> 
<img  src="https://user-images.githubusercontent.com/33378412/230987693-6fb0145c-eeba-4e97-a3f5-a995f141f2df.png" width="320" height="33%">

 </div>


## Installation
```
git clone https://github.com/saba99/Dynamic-NeRF.git
cd D-NeRF
pip install -r requirements.txt
cd torchsearchsorted
pip install .
cd ..
```

## Download Pre-trained Weights
 You can download the pre-trained models from [drive](https://drive.google.com/file/d/1uHVyApwqugXTFuIRRlE4abTW8_rrVeIK/view?usp=sharing) or [dropbox](https://www.dropbox.com/s/25sveotbx2x7wap/logs.zip?dl=0). Unzip the downloaded data to the project root dir in order to test it later. 


## Download Dataset
 You can download the datasets from [drive](https://drive.google.com/file/d/19Na95wk0uikquivC7uKWVqllmTx-mBHt/view?usp=sharing) or [dropbox](https://www.dropbox.com/s/0bf6fl0ye2vz3vr/data.zip?dl=0). Unzip the downloaded data to the project root dir in order to train.  


## Render(Rotate with your Mouse)


              
https://user-images.githubusercontent.com/33378412/230990483-820d2c11-9e71-4cd7-9add-df2ded0f4f1f.mp4





## Test
First download pre-trained weights and dataset. Then, 
```
python run_dnerf.py --config configs/mutant.txt --render_only --render_test
```
This command will run the `mutant` experiment. When finished, results are saved to `./logs/mutant/renderonly_test_799999` To quantitatively evaluate model run `metrics.ipynb` notebook

## Train
First download the dataset. Then,
```
conda activate dnerf
export PYTHONPATH='path/to/D-NeRF'
export CUDA_VISIBLE_DEVICES=0
python run_dnerf.py --config configs/mutant.txt
```
