# Local_AlphaFold_Script_V2.3

# Scripts
1. `alphafold_fast.sh` Nothing to worry about for this script
2. `pred_gpu112.sh` For a node that uses cuda 11 (hpc_v100,hpc_a10,hpc_a100)
modify only two things
 - Line 4: `#SBATCH -J jobname`
 jobname should be the name of your fasta file. Note that the fasta file must end with ".fasta"
 
 - Line 30: `model="multimer"`
 choose between multimer or monomer
 
 3. "Your.fasta" file  
 ##For monomer, prepare a fasta file with your protein sequence
 ```
 >sequence_name
 MRRRRAAAAGGGG
 ```
 ##For multimer, prepare a fasta file with multiple chains
 ```
 >chain A
 MRRRRCHAINA
 >chain B
 MRRRRCHAINB
 ...
 ```
 
 4. After everything is set, `sbatch pred_gpu112.sh` to submit your job
