# Spark's Jupyter session

## Initialization

We need to haver docker running and install the ``jupyter/all-spark-notebook`` with:
```bash
jupyter/all-spark-notebook
```

Then, we define the local folder `<folder>` in which we will add and modify our notebook, and we run a container typing...
docker run -d --name spark-notebook -p 8888:8888 -v C:\Users\gerar\FPDS\Big-Data\hands_on\spark-sql\data\:/work jupyter/all-spark-notebook