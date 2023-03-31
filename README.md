# Local_AlphaFold_Script_V2.3

# Scripts
 1. Copy `pred_gpu112.sh` to your work folder  
 
 2. Input fasta file, `modelname.fasta`  
   - For monomer, prepare a fasta file with your protein sequence
 ```
 >sequence_name
 MRRRRAAAAGGGG
 ```
 
   - For multimer, prepare a fasta file with multiple chains
 ```
 >chain A
 MRRRRCHAINA
 >chain B
 MRRRRCHAINB
 ...
 ```
 
 3. After everything is set, `sbatch pred_gpu112.sh` to submit your job
 ```
 sbatch pred_gpu112.sh modelname modelinfo
 ```
 where `modelname` is the name of your fasta file as in `modelname.fasta` and `modelinfo` can only be `multimer` or `monomer`
 
 4. Enjoy!
