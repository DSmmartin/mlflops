# MLFlops: deep dive into MLOps with MLFlow

## 1. Deploy and setup PostgreSQL database to remote backend

1. Deploy the database
2. Create a database "mlflops"

[Documentation to deploy the database on Azure](https://learn.microsoft.com/en-us/azure/postgresql/single-server/quickstart-create-server-database-portal)


## 2. Create mlflops conda environment base on conda.yml

## 3. Launch mlflow server

```bash
mlflow server --backend-store-uri "postgresql://DATABASENAME.postgres.database.azure.com/mlflops?user=USERNAME@DATABASENAME&password=PASSWORD" --host localhost  --default-artifact-root ./mlflowruns --port 5000
```

## 4. Open mlflow UI

Go to http://localhost:5000



## 4. Launch the experiment example

```bash
python example.py
```

### References

[MLflow documentation](https://mlflow.org/docs/latest/index.html)

[MLflow on Azure](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlflow)

[MLflow on Azure with PostgreSQL](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-use-mlflow#use-postgresql-as-a-backend-store)


## MLFlow References Staging:

[Databricks notebook example](https://docs.databricks.com/_static/notebooks/mlflow/mlflow-model-registry-example.html)

[Medium example](https://medium.com/domino-research/managing-multiple-machine-learning-models-in-production-with-mlflow-and-bridge-168ae58e337)

[YouTube Video: Productionalizing Models through CI/CD Design with MLflow](https://www.youtube.com/watch?v=wpFDsvXORuU)
