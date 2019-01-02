# ice-cores

by Joe Hahn,<br />
jmh.datasciences@gmail.com,<br />
1 January 2019<br />
git branch=master

doodling with historical temperatures inferred from antarctic ice cores...in progress...


### install Anaconda python

Before downloading Anaconda python, first browse https://repo.continuum.io/archive
and select the Anaconda installer that is relevant to your OS (MacOSX in my case)
with a version number matching that used by me (5.3.1), and then download and
execute that installer

    wget https://repo.continuum.io/archive/Anaconda2-5.3.1-MacOSX-x86_64.sh
    chmod +x Anaconda2-5.3.1-MacOSX-x86_64.sh
    ./Anaconda2-5.3.1-MacOSX-x86_64.sh -b -p ./anaconda2

and then use the PYTHON_PATH bash variable to point at the folder where Anaconda python is installed:

    PYTHON_PATH="$(echo $(pwd))"/anaconda2/bin
    $PYTHON_PATH/python --version

and that python v2.7.15 is installed locally


### download ice core data

Download ice core data from http://www.climatedata.info, which appears to contain a nicely
curated archive of climate data:

    mkdir data
    cd data
    wget http://www.climatedata.info/proxies/data-downloads/files/truedownloadAssets/ice-cores-data-pack.zip
    unzip ice-cores-data-pack.zip
    cd ..

