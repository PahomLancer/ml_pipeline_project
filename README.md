# ml_pipeline_project
0 unzip
1 Update DataSchema in ml/data.py and update ml/features.py
2 cd ml_pipeline_project
3 Place your dataset.csv into the data/ directory.
4 python train.py
5 docker build -t cpq-model-api
6 docker run -p 8000:8000 cpq-model-api
7 curl http://localhost:8000/health
8 curl -X 'POST' \
  'http://localhost:8000/predict' \
  -H 'Content-Type: application/json' \
  -d '{"data": [[1.0, 2.0, 3.0], [4.0, 5.0, 6.0]]}'
9 pytest
