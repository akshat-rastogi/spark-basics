# spark-practice

The practice exercises for spark using python. 
Jupyter Notebooks are being used for this exercise and includes how to use basic spark dataframes with spark sql.


## Requirements

The following will be required to use pyspark

- Python 3 (<=3.7)
- Java 
- Scala
- Spark (2.4.6) + Apache hadoop (2.7)
- Jupyter Notebooks

## Installation Steps on Ubuntu

#### Check python version - python3

```
python3
```

We will be using spark 2.4 version which sometimes does not work with python 3.8, so we have to install python 3.7 or lower.


#### Install pip3 

```
sudo apt install python3-pip
```

#### Install Jupyter notebook

```shell
pip3 install jupyter
sudo snap install jupyter
jupyter notebook
```

#### Install Java

```
sudo apt=get update
sudo apt-get install default-jre
```

#### Check java version 

```
java -version
```

Java version used for this project is 11.0.7, but older versions may be supported as well.

#### Install scala

```
sudo apt-get install scala
```

#### Check scala version 

```
scala -version
```

Scala version used for the project is 2.11.12

#### Download Apache Spark 

Spark 2.4.6 + Apache hadoop 2.7
You can find the link to download at this <a href="https://spark.apache.org/downloads.html">https://spark.apache.org/downloads.html</a>

#### Export paths

You will need to set some paths in order to use spark with python

```
export SPARK_HOME='/home/ubuntu/spark-2.4.6-bin-hadoop2.7'
export PATH=$SPARK_HOME:$PATH
export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/lib/py4j-0.10.7-src.zip:$PYTHONPATH
export PYSPARK_DRIVER_PYTHON="jupyter"
export PYSPARK_DRIVER_PYTHON_OPTS="notebook"
export PYSPARK_PYTHON=python3.7
```

#### Check pyspark

```
cd $SPARK_HOME/python
python3
>>>import pyspark
>>>quit()
```

If it doesn't throw any error then pyspark works fine.

#### Load pyspark from anywhere

Use findspark library to load pyspark from any path in python/jupyter notebook

```
pip3 install findspark
python3
>>>import findspark
>>>findspark.init('/home/ubuntu/spark-2.4.6-bin-hadoop2.7')
>>>quit()
```


## Reference


These execrises are created using the tutorial on Udemy by Jose Portilla
(Spark and Python for Big data with pyspark)
