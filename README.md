# CMS_TapeDeletionCampaign_Fall2022
2022-10-11

Repository to keep tracking the second tape deletion campaign of 2022.

## How was created the list
Go to [SWAN](https://swan.cern.ch/), copy the notebook `02_find_tape_containers_PROD.ipynb` in your working directory. 
Select the General Purpose (Analytix) cluster.
![Alt text](/img/screenshot_select_cluster.png)

Open the notebook, click on "Spark clusters connection" and select the following config:
```
spark.driver.memory
   8g
spark.executor.memory
   8g
spark.jars.packages
   org.apache.spark:spark-avro_2.12:3.2.1
```
The last one to ensure you are using the same spark-avro version.

![Alt text](/img/screenshot_select_spark_config.png)

## How to extract the list
```
$ tar -xvzf AllContainersAtTapeSites.tar.gz
```
