## Intro
Are you tired of not being able to publish files not created by CRAB using CRAB? Of course you are.

## Setup
0. Check out this repository
1. `cmsrel CMSSW_7_4_1_patch1; cd CMSSW_7_4_1_patch1/src` or use your favorite release
2. `cmsenv; source /cvmfs/cms.cern.ch/crab3/crab.sh`
3. Edit filelist.txt to have one file to publish per line (each crab job publishes one file).
   Note that `/hadoop/cms/store/user/namin/asdf` must be input as `/store/user/namin/asdf` as this is what xrootd expects.
4. Edit the `name` and `filelist` variables in `cfg.sh`
5. `crab submit cfg.sh`

## To do
* Change script so that we can publish arbitrary root files (non-EDM files)
