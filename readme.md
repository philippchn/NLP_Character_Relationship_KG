01_data_pipeline.ipynb
  -> creates candidate_examples.csv
  -> optionally consumes candidate_examples_llm_labeled.csv if it already exists
  -> writes train.csv, dev.csv, test.csv

01_llm_judge_colab_gpu_minimal.ipynb
  -> reads candidate_examples.csv
  -> runs the LLM Judge on Colab GPU
  -> writes candidate_examples_llm_labeled.csv

02_models.ipynb
  -> trains models using the split produced by 01

03_graph_generation.ipynb
  -> builds KG edges and HTML graphs

04_evaluation_and_comparing.ipynb
  -> summarizes model and graph outputs