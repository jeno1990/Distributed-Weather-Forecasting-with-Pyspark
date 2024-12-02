**Distributed Weather Forecasting**
This project leverages Apache Spark and Hadoop to process and analyze large-scale weather data in a distributed environment.

Features
Distributed data processing using Apache Spark and Hadoop.
Scalable infrastructure for weather forecasting tasks.

**Prerequisites**
Before running this project, ensure you have the following installed and configured:

Python 3.7 or later
Apache Spark
Hadoop with HDFS
PySpark library

**Installation**
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/Distributed-Weather-Forecasting.git
cd Distributed-Weather-Forecasting
Install the required Python packages:

bash
Copy code
pip install -r requirements.txt
Start the Hadoop Distributed File System (HDFS):

bash
Copy code
start-dfs.sh
Start the Spark master and worker nodes:

bash
Copy code
start-all.sh

**Setting Up the Data**
Place the weather dataset in the HDFS directory:
https://www.kaggle.com/sudalairajkumar/daily-temperature-of-major-cities

bash
Copy code
hdfs dfs -put /path/to/your/dataset.csv /hdfs/destination/path
Confirm the file has been uploaded to HDFS:

bash
Copy code
hdfs dfs -ls /hdfs/destination/path
Running the Project
Start a Jupyter Notebook server or run the script:

bash
Copy code
jupyter notebook
Open the notebook weather_forcast_big_data.ipynb.

Execute the cells in order to initialize Spark, process the data, and run analysis.

If the the worker is not able to read data from master add this code to core-site.xml and hdfs-site.xml
**core-site.xml**
    <property>
        <name>fs.defaultFS</name>
        <value>hdfs://0.0.0.0:9000</value>
    </property>
    <property>
        <name>hadoop.http.staticuser.user</name>
        <value><**username**></value>
    </property>
**hdfs-site.xml**
    <property>
        <name>dfs.namenode.rpc-bind-host</name>
        <value>0.0.0.0</value>
    </property>
