mlflow server \
  --backend-store-uri sqlite:////root/mlflow_data/db/mlflow.db \
  --default-artifact-root file:///root/mlflow_data/artifacts \
  --host 0.0.0.0 \
  --port 5000 \
  --allowed-hosts mlflow.labs.itmo.loc,10.100.0.8,10.100.0.9,localhost,127.0.0.1 \
  --cors-allowed-origins http://mlflow.labs.itmo.loc,http://10.100.0.9



# С машины 10.100.0.9
curl -v http://10.100.0.8:5000 -H "Host: mlflow.labs.itmo.loc" 

-------------------------------------------------------------------

