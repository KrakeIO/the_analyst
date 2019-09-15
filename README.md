# A simple web service that takes in a bunch of parameters and determines the probability that a large dip will recover

## Running Jupyter NoteBook  
  ```
  # Python 2.7
  source venv/bin/activate
  ipython notebook 
  ```

## Pre-requisities
- Python 2.7
- pip

Installing Python 2.7
```
brew install python
```

Install PIP
```
wget https://bootstrap.pypa.io/get-pip.py
python get-pip.py
```

## Setting up

Setting locale
  ```
  # Add the following two lines in ~/.bash
  export LC_ALL=en_US.UTF-8
  export LANG=en_US.UTF-8
  ```

Setting MySql path
  ```
  export PATH=$PATH:/usr/local/mysql/bin
  ```

Installing virtual environment
  ```
  pip install virtualenv 

  # Run to make sure its been installed
  which virtualenv
  ```

Setting up virtual environment
  ```
  mkdir venv
  virtualenv venv
  ```

Activating into virtual environment
  ```
  source venv/bin/activate
  ```

Install requirements
  ```
  pip install -r requirements.txt
  python -m textblob.download_corpora
  ```

## Running webserver
  We expose our trained model as a webservice to be called externally
  ```
  # Running the webservice at port 10003
  python service/web_server.py 10003

  # using make file
  make web
  ```