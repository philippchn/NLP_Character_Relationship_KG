# Project structure
Two of the notebooks were run on Colab GPU. For this a google drive mount was used for the input and output data

01_data_pipeline.ipynb
  -> creates candidate_examples.csv
  -> optionally consumes candidate_examples_llm_labeled.csv if it already exists
  -> writes train.csv, dev.csv, test.csv

01.5_llm_judge_colab_gpu.ipynb
  -> reads candidate_examples.csv
  -> runs the LLM Judge on Colab GPU
  -> writes candidate_examples_llm_labeled.csv

02_models.ipynb
  -> trains models using the split produced by 01

02.5_transformer_colab.ipynb
  -> runs DistilBERT on Colab GPU

03_graph_generation.ipynb
  -> builds KG edges and HTML graphs

04_evaluation_and_comparing.ipynb
  -> summarizes model and graph outputs