# 🚲 Bike Sharing Dataset

## 📌 Overview

The **Bike Sharing Dataset** contains historical bike rental data from the Capital Bikeshare system in Washington, D.C., USA, covering the years **2011 and 2012**.

The dataset was collected and aggregated on both hourly and daily bases, with corresponding weather and seasonal information. It helps analyze how environmental and seasonal conditions influence bike rental demand.

**Dataset Author:** Hadi Fanaee-T
**Institution:** Laboratory of Artificial Intelligence and Decision Support (LIAAD), University of Porto, INESC Porto
**Location:** Campus da FEUP, Rua Dr. Roberto Frias, 378, 4200-465 Porto, Portugal

---

## 🌍 Background

Bike-sharing systems are a modern generation of traditional bicycle rental services in which the entire process of membership, rental, and return is automated.

Users can rent a bicycle from one location and return it at another, making transportation more flexible and accessible.

Currently, bike-sharing systems play an important role in addressing:

- Urban traffic congestion
- Environmental sustainability
- Public health and physical activity
- Sustainable transportation

These systems also generate valuable data for research. Unlike traditional transportation services such as buses and subways, bike-sharing systems explicitly record travel duration, departure locations, and arrival locations.

This makes bike-sharing systems a type of **virtual sensor network** that can be used to understand urban mobility and identify important events occurring within a city.

---

## 📊 Dataset Description

The dataset contains historical rental records from the Capital Bikeshare system in Washington, D.C., USA.

- **Time Period:** 2011–2012
- **Location:** Washington, D.C., USA
- **Data Aggregation:** Hourly and Daily
- **Weather Information:** Extracted from Freemeteo
- **Source of Rental Data:** Capital Bikeshare

The dataset combines bike rental information with environmental and seasonal variables to study rental demand patterns.

### Dataset Files

| File         | Description                          | Records |
| ------------ | ------------------------------------ | ------: |
| `hour.csv`   | Bike rental counts aggregated hourly |  17,379 |
| `day.csv`    | Bike rental counts aggregated daily  |     731 |
| `Readme.txt` | Dataset documentation                |       — |

---

## 🎯 Associated Tasks

The dataset supports two major research tasks.

### 1. Regression

Predict the number of rented bicycles on an hourly or daily basis using environmental and seasonal conditions.

Potential influencing factors include:

- Temperature
- Feeling temperature
- Humidity
- Wind speed
- Weather conditions
- Season
- Month
- Day of the week
- Hour of the day
- Holidays and working days

The target variable is `cnt`, representing the total number of rented bicycles.

### 2. Event and Anomaly Detection

Bike rental counts can also be influenced by unusual events occurring in the city.

For example, the rental count on October 30, 2012, may be affected by Hurricane Sandy.

Such events can be identified using external information sources and search engines, making this dataset useful for validating event detection and anomaly detection algorithms.

---

## 📝 Dataset Attributes

Both `hour.csv` and `day.csv` contain the following attributes, except `hr`, which is available only in `hour.csv`.

| Attribute    | Description                                             |
| ------------ | ------------------------------------------------------- |
| `instant`    | Record index                                            |
| `dteday`     | Date                                                    |
| `season`     | Season (1: Spring, 2: Summer, 3: Fall, 4: Winter)       |
| `yr`         | Year (0: 2011, 1: 2012)                                 |
| `mnth`       | Month (1 to 12)                                         |
| `hr`         | Hour of the day (0 to 23); available only in `hour.csv` |
| `holiday`    | Indicates whether the day is a holiday                  |
| `weekday`    | Day of the week                                         |
| `workingday` | 1 if neither weekend nor holiday, otherwise 0           |
| `weathersit` | Weather situation category                              |
| `temp`       | Normalized temperature in Celsius                       |
| `atemp`      | Normalized feeling temperature in Celsius               |
| `hum`        | Normalized humidity                                     |
| `windspeed`  | Normalized wind speed                                   |
| `casual`     | Count of casual users                                   |
| `registered` | Count of registered users                               |
| `cnt`        | Total number of rented bicycles                         |

### Weather Situation (`weathersit`)

| Value | Weather Condition                                                                       |
| ----- | --------------------------------------------------------------------------------------- |
| 1     | Clear, Few clouds, Partly cloudy                                                        |
| 2     | Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist                            |
| 3     | Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds |
| 4     | Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog                              |

### Normalized Variables

The environmental variables are normalized as follows:

| Variable    | Description                    | Normalization            |
| ----------- | ------------------------------ | ------------------------ |
| `temp`      | Temperature in Celsius         | Divided by 41 (maximum)  |
| `atemp`     | Feeling temperature in Celsius | Divided by 50 (maximum)  |
| `hum`       | Humidity                       | Divided by 100 (maximum) |
| `windspeed` | Wind speed                     | Divided by 67 (maximum)  |

---

## 📈 Target Variable

The primary target variable for regression is:

### `cnt` — Total Bike Rental Count

It represents the total number of rented bicycles, including both casual and registered users.

The relationship is:

```text
cnt = casual + registered
```

This variable can be used to develop predictive models for estimating bike rental demand.

---

## 🔍 Potential Research Applications

The dataset can be used for:

1. Bike rental demand prediction.
2. Time-series analysis of rental patterns.
3. Seasonal demand analysis.
4. Weather impact analysis.
5. Urban mobility analysis.
6. Event and anomaly detection.
7. Regression model evaluation.
8. Transportation demand forecasting.

---

## 📚 Data Sources

**Capital Bikeshare System Data**

[http://capitalbikeshare.com/system-data](http://capitalbikeshare.com/system-data)

**Weather Information**

[http://www.freemeteo.com](http://www.freemeteo.com)

**Holiday Schedule**

[http://dchr.dc.gov/page/holiday-schedule](http://dchr.dc.gov/page/holiday-schedule)

---

## 📜 License and Citation

If you use this dataset in research publications, cite the following publication:

**Fanaee-T, Hadi, and Gama, Joao.**

"Event labeling combining ensemble detectors and background knowledge."

*Progress in Artificial Intelligence* (2013), Springer Berlin Heidelberg, pp. 1–15.

**DOI:** [https://doi.org/10.1007/s13748-013-0040-3](https://doi.org/10.1007/s13748-013-0040-3)

### BibTeX Citation

```bibtex
@article{fanaee2013event,
    year={2013},
    issn={2192-6352},
    journal={Progress in Artificial Intelligence},
    doi={10.1007/s13748-013-0040-3},
    title={Event labeling combining ensemble detectors and background knowledge},
    url={http://dx.doi.org/10.1007/s13748-013-0040-3},
    publisher={Springer Berlin Heidelberg},
    keywords={
        Event labeling,
        Event detection,
        Ensemble learning,
        Background knowledge
    },
    author={Fanaee-T, Hadi and Gama, Joao},
    pages={1-15}
}
```

---

## 📧 Contact

For further information regarding the dataset, contact:

**Hadi Fanaee-T**
Email: [hadi.fanaee@fe.up.pt](mailto\:hadi.fanaee@fe.up.pt)

---

\<p align="center">   \<strong>Bike Sharing Dataset — Understanding Urban Mobility Through Data\</strong> \</p>



