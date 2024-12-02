
## Distributed Weather Forecasting

This project leverages Apache Spark and Hadoop to process and analyze large-scale weather data in a distributed environment.

## Features
- Distributed data processing using Apache Spark and Hadoop.
- Scalable infrastructure for weather forecasting tasks.

## Prerequisites
Before running this project, ensure you have the following installed and configured:
- Apache Spark
- Hadoop with HDFS

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Distributed-Weather-Forecasting.git
   cd Distributed-Weather-Forecasting
## Install the required Python packages:
pip install -r requirements.txt

Update the core-site.xml and hdfs-site.xml files with the following properties:

core-site.xml
```xml
<pre> 
   <property>
    <name>fs.defaultFS</name>
    <value>hdfs://0.0.0.0:9000</value>
</property>
<property>
    <name>hadoop.http.staticuser.user</name>
    <value>--username--</value>
</property>
   </pre>
```
hdfs-site.xml

```xml
<property>
    <name>fs.defaultFS</name>
    <value>hdfs://0.0.0.0:9000</value>
</property>
```

##Start the Hadoop Distributed File System (HDFS):

```bash
start-dfs.sh
```
Start the Spark master and worker nodes:

```bash
start-all.sh
```

##Dataset
This project uses the Daily Temperature of Major Cities dataset, which can be downloaded from Kaggle:
https://www.kaggle.com/sudalairajkumar/daily-temperature-of-major-cities

Setting Up the Data
Download the dataset and place it in your local directory.

Upload the dataset to HDFS:

```bash

hdfs dfs -put /path/to/daily-temperature.csv /hdfs/destination/path
```
Confirm the file has been uploaded to HDFS:

```bash

hdfs dfs -ls /hdfs/destination/path
```

Running the Project
Start a Jupyter Notebook server or run the script:

```bash
jupyter notebook
```
Open the notebook weather_forcast_big_data.ipynb.

Execute the cells in order to initialize Spark, process the data, and run analysis.

