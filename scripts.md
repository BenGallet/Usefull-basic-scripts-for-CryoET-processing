# Basic Usefull scripts

## IMOD:

  to open all the .mrc files of a folder, one by one  
$ for i in *.mrc;do 3dmod -W $i;done

  to reorder all tilt in a tilt-serie  
$ newstack -reorder 1 –mdoc –input ./ts01.mrc –output ./reordered/ts01_reordered.mrc

## AreTomo2:

to reconstruct ts01.mrc  
$ AreTomo2 –InMrc ./ts01.mrc –OutMrc ./rec/tomo.mrc –VolZ 1200 –OutBin 4 –Patch 5 5 –TiltCor 1 –WBP 1

## membrain-seg:

  to activate membrain env  
$ conda activate "membrain-seg_env"

  to segment tomo.mrc  
$ membrain segment --tomogram-path tomo.mrc --ckpt-path ∼/MemBrain_seg_v10_alpha.ckpt --store-connected-components --rescale-patches

  to segment all .mrc files in one folder  
$ for i in *.mrc; do membrain segment --tomogram-path $i --ckpt-path ∼/MemBrain_seg_v10_alpha.ckpt --store-connected-components --rescale-patches; done

## CryoCARE:

  to activate cryocare env  
$ conda activate "cryocare_env"

  to train cryocare NN  
$ 


## 
