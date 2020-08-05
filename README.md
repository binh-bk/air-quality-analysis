# air-quality-analysis
Jupyter notebooks and Python code for analyzing air quality (fine particles, PM<sub>2.5</sub>) 

# Table of contents

#### <a href="#1">1. Basic data visualization</a>
#### <a href="#2">2. Correlation of PM<sub>2.5</sub></a>
#### <a href="#2">2. Correlation of PM<sub>2.5</sub></a>
#### <a href="#2">2. Correlation of PM<sub>2.5</sub></a>
#### <a href="#2">2. Correlation of PM<sub>2.5</sub></a>
#### <a href="#assesing_data">3. Data Exploratory</a>
#### <a href="#credit">4. Credits</a>


<a id="1"></a>
## 1. Basic data visualization
- introduce to basic setup of folder, install `pandas`, `matplotlib`, `seaborn` (using `pip` for Python package), `Anaconda` is a good choice if you are using Windows (or even Mac, Linux). Alternatively, try out [**Google Colaboratory**](https://colab.research.google.com/)
- basic use of those tools (clean, explore, plot, interpret)
- work with a CSV file from [Airnow.gov](https://www.airnow.gov/international/us-embassies-and-consulates/)
- here are some graphs produced from this exercise
  - basic line chart
  <p align="center">
    <img style="width: 100%;" src="img/2020Jul_hanoi.png"/>
  </p>
  
  - line chart with a band for standard deviation
  <p align="center">
    <img style="width: 100%" src="img/2020Jul-pm25.png"/>
  </p>
  - pie chart with Air Quality Index (AQI) 
  <p align="center">
    <img style="max-width: 100%;" src="img/2020Jul-AQI.png"/>
  </p>

<a id="2"></a>
## 2. Correlation of PM<sub>2.5</sub>
<a id="2.1"></a>
### 2.1 Correlation of PM<sub>2.5</sub> with time
- continue to work with the .CSV file from **AirNow.Gov** to explore the correlation between PM<sub>2.5</sub> and time such as:
  - peak-traffic hours vs. non-peak traffic hours
  - weekends vs. weekdays
  - variation of each months
- here is some graphs produced from this exercise
  <p align="center">
    <img style="width: 70%" src="img/2020Jul-peakhours.png"/>
  </p>
- a summary graph of this dataset
  <p align="center">
    <img style="width: 70%" src="img/2020Jul-pm25-time.png"/>
  </p>

<a id="2.2.1"></a>
### 2.2 Correlation of PM<sub>2.5</sub> with wind and temperature (data cleaning)
- explore data source (specifically working with archieved meteorologcal data from [NOAA.GOV](ncei.noaa.gov)
- clean the data (which is formatted with Integrated Surface Data (ISD) style)
- use `windrose` package to make windrose plot

  <p align="center">
    <img style="width: 70%" src="img/2020Jul_windrose_noibai_hadong.png"/>
  </p>

<a id="2.2.2"></a>
### 2.2 Correlation with wind and temperature (analysis)
- explore correlation between meteorological paramters to observed PM<sub>2.5<sub> concentration such wind, temperature, height above ground
- capture espisode and examine relevant inputs with PM<sub>2.5</sub>
- some examples from this exercise
  - correlation graph:
  <p align="center">
    <img src="img/2020Jul_corr_pm25.png"/>
  </p>
  - what method in *that* correlation?
    <p align="center">
    <img src="img/2020Jul_corr_method.png"/>
    </p>
  - a high PM<sub>2.5</sub> and a cloudy day
    <p align="center">
    <img src="img/2020Jul_mixing_feb.png"/>
    </p>
  - or, I want to see other inputs such as.. 
  
    <p align="center">
    <img src="img/2020Jul_all_params.png"/>
    </p>
<a id="2.3"></a>
### 2.3 Correlation with MERRA-2 data
- work with [MERRA-2](https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/) reanalysis data from NASA
- find the correlation from main groups (single level, surface turbulent flux, aerosols mixing ratio) and PM<sub>2.5</sub>
- here is the 3 summary graphs:
  - Single level diagnosis
  <p align="center">
    <img src="img/2020Aug-SLV-subplot.png"/>
  </p>
  
  - surface turbulent flux
  <p align="center">
    <img src="img/2020Aug-FLX-subplot.png"/>
  </p>
  
  - Aerosol mixing:
  <p align="center">
    <img src="img/2020Aug-AER-subplot.png"/>
  </p>

<a id="todo"></a>
# TODO
## building prediction


## tools

<a id="credit"></a>
## Credits:
- some of the writing and coding are carried out while I were working with [PAM Air](pamair.org) project.  I appreciate the flexiblity from the management so that I can make this happen.

## If this work is helpful to your research
- Admittedly, citing Github repository or other open project is new, but if this work is helpful for your work, I would appreciate the attribution, a link or a word.
- To cite this work, use this `Binh Nguyen, Air Quality Analysis, GitHub repository: https://github.com/binh-bk/air-quality-analysis`
