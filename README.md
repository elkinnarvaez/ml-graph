# Project 3: Big Data

## Data cleaning
Copiar datos en el cluster
```
hadoop fs -copyFromLocal /home/maria_dev/ml-graph/data/Chicago_Crimes_2012_to_2017.csv /user/maria_dev/ml-graph/data
```
Ejecutar la limpieza de datos
```
sudo /usr/hdp/current/spark2-client/bin/spark-submit data_cleaning.py /user/maria_dev/ml-graph/data/Chicago_Crimes_2012_to_2017.csv /user/maria_dev/ml-graph/data/cleaned_data
```

## Machine learning
```
sudo /usr/hdp/current/spark2-client/bin/spark-submit machine_learning.py
```
```
sudo /usr/hdp/current/spark2-client/bin/spark-submit --packages graphframes:graphframes:0.8.2-spark2.4-s_2.11 machine_learning.py
```
```
sudo /usr/hdp/current/spark2-client/bin/spark-submit --jars graphframes-0.8.2-spark2.4-s_2.11.jar machine_learning.py
```