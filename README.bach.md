1. Create input for w2vf
1.1. wvocab - use the freq gen function in dep_colloc
1.2. cvocab - use the freq gen function in dep_colloc
1.3. dep.contexts - use the generate_syn_colloc_df function in dep_colloc then convert the df to the dep.contexts
1.4. Remember to compile the repo by running the command: make

2. Train the model (terminal)
2.1. cd to the word2vecf folder
2.2. command
./word2vecf \
-train /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/dep.contexts \
-wvocab /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/wvocab \
-cvocab /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/cvocab \
-output /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/dim10vecs \
-size 10 \
-negative 15 \
-threads 10 \
-dumpcv /home/volt/bach/pilot_data/COHA/lemma_emb/w2vf/dep_w2v/dim10context-vecs


