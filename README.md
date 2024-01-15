# Spark and wsl install with pycharm
Instalation proccess of wsl (Ubuntu distribution), spark and pycharm IDE on win 11

## 1. wsl installation
* search for *Powershell* on the win11 searchbar and open it
* on Powershell type:

  ```
  wsl --install -d Ubuntu
  ```
* this will install Ubuntu distribution
* after installation linux will ask for username and password
* ! when typing password letters/numbers won't show but they will be inputed
* after installation update and upgrade linux by typing:

  ```
  sudo apt update -y
  ```

* enter your user password you've just inputed after linux installation

  ```
  sudo apt upgrade
  ```

## 2. jdk installation
* on linux use:

  ```
  sudo apt install openjdk-8-jdk -y
  ```

* after installation open nano editor by:

  ```
  nano~/.bashrc
  ```
  
* srcoll down to the bottom of the file with arrows and paste:
  
  ```
  export JAVA_HOME=”/usr/lib/jvm/java-8-openjdk-amd64”  
  ```
  
* to close nano editor use *ctrl+x* then *y* and *enter*

## 3. spark installation
* on linux use commands:
  
  ```
  mkdir Ubuntu
  ```
  ```
  cd Ubuntu
  ```
  ```
  mkdir Downloads
  ```
  ```
  cd Downloads
  ```
  
* download current version of spark to Download folder, if needed change spark and hadoop versions
  
  ```
  wget https://dIcdn.apache.org/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz
  ```
  
* create Programs folder and unpack spark to it
  
  ```
  cd ..
  ```
  ```
  mkdir Programs
  ```
  ```
  tar -xvf Downloads/spark-3.5.0-bin-hadoop3.tgz -C Programs
  ```

  * remeber to update spark/hadoop vesions if you downloaded other ones
* open nano editor and paste variable, remember to set your own user name into the path under 'YOU' and also right spark/hadoop versions
  
  ```
  nano~/.bashrc
  ```
  
  ```
  export SPARK-HOME=”/mnt/c/Users/YOU/Ubuntu/Programs/spark-3.5.0-bin-hadoop3”
  ```
## 4. python pip and pyspark installation
* since Ubuntu already has python 3.10 preinstalled we need to install pip
* type this command to install pip for linux
  
  ```
  sudo apt install python3-pip -y
  ```

* install pyspark on linux using pip
  
  ```
  sudo pip install pyspark
  ```

* check pyspark installation by:
  
  ```
  pyspark
  ```

* use *ctrl+z* to exit pyspark console
## 5. install pycharm for linux
* open Downloads folder and download pycharm 2023.3.2 version and exit the folder:
  
  ```
  cd Downloads
  ```
  ```
  wget https://download.jetbrains.com/python/pycharm-community-2023.3.2.tar.gz
  ```
  ```
  cd ..
  ```

* unpack Pycharm to Programs folder:
  
  ```
  tar -xvf Downloads/pycharm-community-2023.3.2.tar.gz -C Programs
  ```

* after unpacking open Pycharm:
  
  ```
  Programs/pycharm-community-2023.3.2/bin/pycharm.sh
  ```

## 6. some additional commands for win11 powershell:
* starting wsl on windows, open powershell and type:\
  ```
  wsl
  ```
* this will start default linux distribution
  
* list of distribution installed on win11:
  ```
  wsl --list
  ```
* uninstall linux distribution and all its files, in this case Ubuntu:
  ```
  wsl --unregister Ubuntu
  ```

  

  
