# Project Overview

### Initial Problem Statement :book:

Based on the dataset provided in Kaggle on 2015 Traffic data, use the appropriate algorithms and models to find out the top 5 most obvious patterns from this data

---

**Jupyter Notebook Organization**

The Jupyter notebook in named `ocbc_Hack_it-version2` . 

----

**Data Dictionary**

To facilitate understanding of column headers and data values, reference document '2001 Traffic Management Guide, Chapter 6' is consulted. This reference document, titled `2001_TMG_Chapter_6` is also provided in the repository for ease of reference.

The data dictionaries for the two datasets below summarizes data understanding regarding the relevant variables used for the two datasets, where the column headers are not self-explanatory and hence potentially difficult to interpret.

**Station data**

| Column                                 | Description                                                  |
| -------------------------------------- | ------------------------------------------------------------ |
| concurrent_route_signing               | Code same as Posted Route Signing for concurrent route if there is one |
| concurrent_signed_route_number         | Code same as Posted Signed Route Number for concurrent route if there is one |
| fips_state_code                        | Code for the states                                          |
| method_of_data_retrieval               | 1 = Not automated (manual)<br />2 = Automated (telemetry)    |
| method_of_traffic_volume_counting      | 1 = Human observation (manual)<br/>2 = Portable traffic recording device<br/>3 = Permanent automatic traffic recorder (ATR) |
| method_of_truck_weighing               | 1 = Portable static scale<br/>2 = Chassis-mounted, towed static scale<br/>3 = Platform or pit static scale<br/>4 = Portable weigh-in-motion system<br/>5 = Permanent weigh-in-motion system |
| method_of_vehicle_classification       | 1 = Human observation (manual) vehicle classification 2 = Portable vehicle classification device<br/>3 = Permanent vehicle classification device |
| primary_purpose                        | E = Enforcement purposes (e.g., speed or weight enforcement)<br/>I = Operations purposes in support of ITS initiatives L = Load data for pavement design or pavement management purposes O = Operations purposes but not ITS<br/>P = Planning or traffic statistics purposes R = Research purposes (e.g., LTPP) |
| sample_type_for_traffic_volume         | T = Station used for Traffic Volume Trends<br/>N = Station not used for Traffic Volume Trends |
| sample_type_for_truck_weight           | B = Station used for TMG sample and Strategic Highway Research Program (SHRP) Long Term Pavement Performance (LTPP) sample<br/>L = Station used for SHRP/LTPP sample (but not TMG sample)<br/>T = Station used for TMG sample (but not SHRP/LTPP sample)<br/>N = Station not used for any of the above |
| sample_type_for_vehicle_classification | H = Station used for Heavy Vehicle Travel Information System<br/>N = Station not used for Heavy Vehicle Travel Information System |
| second_type_of_sensor                  | If there are two types of sensors at the station, code the second using the same codes as Type of Sensor. Otherwise, code "N" for none. |



**Traffic Data**

| Column                   | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| direction_of_travel      | 1 - North<br />2 - Northeast<br />3 - East<br />4 - Southeast<br />5 - South<br />6 - Southwest<br />7 - West<br />8 - Northwest<br />9 - North-South or Northeast-Southwest combined (ATR stations only)<br />0 - East-West or Southeast-Northwest combined (ATR stations only) |
| direction_of_travel_name | directions                                                   |
| functional_class         | 3R - Rural: Principal Arterial - Other<br />1U - Urban: Principal Arterial - Interstate<br />4R - Rural: Minor Arteria<br />2U - Urban: Principal Arterial - Other Freeways or Expressways<br />3U -  Urban: Principal Arterial - Other<br />4U - Urban: Minor Arterial<br />1R - Rural: Principal Arterial - Interstate<br />5R - Rural: Major Collector<br />6R - Rural: Minor Collector<br />5U - Urban: Collector<br />7R - Rural: Local System'<br />7U - Urban: Local System |
| functional_class_name    | name of highway code                                         |



____

**Observations**

Corresponding observations are documented within the jupyter notebook in markdown cells marked with `Observation number`. Data visualizations and a model (K-Means clustering) is used to derive the observations.

**Reframed Problem Statement**

Based on the insights gathered from the observations, the problem statement is reframed and several models built to predict traffic volume. These are evaluated to select the best predictive model for subsequent model tuning. All model performance metrics are recorded within the notebook.

------

Note:

Datasets are within the `archive` folder.

In interest of time, the best performing model is saved as `bestModel.sav` pickle file. 

Alternative code cells are provided along with prompters within the Jupyter notebook for readers to load the pickled model should the tuning of the model take too long to complete.

___

