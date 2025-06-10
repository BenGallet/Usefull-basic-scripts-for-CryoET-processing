# Basic Usefull scripts

## IMOD:

  to open all the .mrc files of a folder, one by one  
_$ for i in *.mrc;do 3dmod -W $i;done_

  to reorder all tilt in a tilt-serie  
_$ newstack -reorder 1 –mdoc –input ./ts01.mrc –output ./reordered/ts01_reordered.mrc_

## AreTomo2:

to reconstruct ts01.mrc  
_$ AreTomo2 –InMrc ./ts01.mrc –OutMrc ./rec/tomo.mrc –VolZ 1200 –OutBin 4 –Patch 5 5 –TiltCor 1 –WBP 1_

## membrain-seg:

  to activate membrain env  
_$ conda activate "membrain-seg_env"_

  to segment tomo.mrc  
_$ membrain segment --tomogram-path tomo.mrc --ckpt-path ∼/MemBrain_seg_v10_alpha.ckpt --store-connected-components --rescale-patches_

  to segment all .mrc files in one folder  
_$ for i in *.mrc; do membrain segment --tomogram-path $i --ckpt-path ∼/MemBrain_seg_v10_alpha.ckpt --store-connected-components --rescale-patches; done_

## CryoCARE:

  to activate cryocare env  
_$ conda activate "cryocare_env"_

  to train cryocare NN  
_$  _


## Scipion-em


