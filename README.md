# UD-MFT

Uniform and Deformable Multi-fish Tracking (UD-MFT) is a benchmark for multi-fish real-time tracking in the farming.

UD-MFT provides box and identity annotations. It contains training(annotations public) and testing(annotations public). 

<div align="center"><img src="https://ars.els-cdn.com/content/image/1-s2.0-S095741742402520X-gr2.jpg" ></div>
</br>

## Paper (ESWA)
[Uniformity and deformation: A benchmark for multi-fish real-time tracking in the farming](https://www.sciencedirect.com/science/article/pii/S095741742402520X)

## Dataset
Download the dataset from [Baidu Drive](https://pan.baidu.com/s/1ZReJYWJNdJjGcyBiPUb16g?pwd=1234) (code:1234).

Organize as follows:
~~~
{UD-MFT ROOT}
|-- UD-MFT
|   |-- train
|   |   |-- cruise1
|   |   |   |-- img1
|   |   |   |   |-- 000001.PNG
|   |   |   |   |-- ...
|   |   |   |-- gt
|   |   |   |   |-- gt.txt            
|   |   |   |-- seqinfo.ini
|   |   |-- ...
|   |-- test
|   |   |-- ...
~~~
We align our dataset annotations with MOT, so each line in  gt.txt contains:
~~~
<frame>, <id>, <bb_left>, <bb_top>, <bb_width>, <bb_height>, <confidence>, <class>
~~~



## Evaluation

| Tracker     |   HOTA  |   DetA  |   AssA  |   MOTA  |   IDF1  |
|-------------|---------|---------|---------|---------|---------|
| SORT		    |   32.81 | 56.26	  | 19.35	  | 66.76	  | 30.69	  | 
| IOUTrack	  | 	35.24 | 58.92	  | 21.19	  | 71.57	  | 34.15	  | 
| ByteTrack	  | 	35.62 | 52.25	  | 24.84	  | 56.48	  | 38.17	  | 
| OCSort	    | 	39.64 | 55.39	  | 28.44	  | 70.82	  | 46.79	  | 
| CenterTrack	| 	36.47 | 58.43	  | 22.87	  | 74.25	  | 37.35	  | 
| DeepSORT	  | 	25.65 | 61.35	  | 10.81	  | 69.68	  | 21.50	  | 
| FairMOT	    | 	16.31 | 29.01	  | 9.45	  | 31.40	  | 15.58	  | 
| GTR         | 	30.97 | 49.86   |   19.41  |   60.18  |  32.93  |   
| TraDes	    |   38.46 |	60.47   |  24.53  |	 77.74 	| 	39.77 |
| QDTrack     |   41.55 | 62.59   |   27.66  |   80.22  |  45.31   |

## Agreement
- The annotations of UD-MFT are licensed under a [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/).
- The dataset of UD-MFT is available for **non-commercial** research purposes only.
- All videos and images of UD-MFT are obtained from the fish farming. 

## Acknowledgement  
 
The evaluation metrics and code are from [MOT Challenge](https://motchallenge.net/) and [TrackEval](https://github.com/JonathonLuiten/TrackEval).
Thanks for their wonderful and pioneering works !
  
