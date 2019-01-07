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
    ./anaconda2/bin/python --version

with the last line in the above indicating that python v2.7.15 was installed locally.


### download ice core data

Download and unzip data from http://www.climatedata.info, which appears to contain a nicely
curated archive of climate data:

    mkdir data; cd data; mkdir ice_cores; cd ice_cores
    wget http://www.climatedata.info/proxies/data-downloads/files/truedownloadAssets/ice-cores-data-pack.zip
    unzip ice-cores-data-pack.zip; cd ..
    mkdir forcing; cd forcing
    wget http://www.climatedata.info/forcing/data-downloads/files/truedownloadAssets/forcing.zip
    unzip forcing.zip
    mkdir Albedo; cp Albdeo.zip Albedo/.; cd Albedo; unzip Albdeo.zip; cd ..
    mkdir Milankovitch; cp Milankovitch.zip Milankovitch/.; cd Milankovitch; unzip Milankovitch.zip; cd ..
    mkdir Oscillations; cp Oscillations.zip Oscillations/.; cd Oscillations; unzip Oscillations.zip; cd ..
    mkdir Radio-sonde; cp Radio-sonde.zip Radio-sonde/.; cd Radio-sonde; unzip Radio-sonde.zip; cd ..
    mkdir Sunspots; cp Sunspots.zip Sunspots/.; cd Sunspots; unzip Sunspots.zip; cd ..



### start jupyter

    ./anaconda2/bin/jupyter notebook
    
and execute the ics_cores.ipynb notebook...

