1. Create input for w2vf
  * remember to first compile the repo by running the command: make
  * wvocab - use the freq gen function in dep_colloc
  * cvocab - use the freq gen function in dep_colloc
  * dep.contexts - use the generate_syn_colloc_df function in dep_colloc then convert the df to the dep.contexts

2. Train the model (terminal)
* cd to the word2vecf folder
* command
```
./word2vecf \
-train /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/dep.contexts \
-wvocab /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/wvocab \
-cvocab /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/cvocab \
-output /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/dim10vecs \
-size 10 \
-negative 15 \
-threads 10 \
-dumpcv /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/dim10context-vecs
```
