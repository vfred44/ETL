### Data

###### Metadata about air quality:

[Eesti välisõhu kvaliteet](http://airviro.klab.ee/)

| Attr  | example value | unit    | Description                 |
| ----- | ------------- | ------- | --------------------------- |
| SO2   | 0,23          | µg/m³ | Vääveldioksiid            |
| NO2   | 0,02          | µg/m³ | Lämmastikdioksiid          |
| CO    | 0,24          | mg/m³  | Süsinikoksiid              |
| O3    | 70,05         | µg/m³ | Osoon                       |
| PM10  | 8,55          | µg/m³ | Peened osakesed             |
| PM2.5 | 4,72          | µg/m³ | Eriti peened osakesed       |
| TEMP  | 9,72          | C       | Temperatuur                 |
| WD10  | 204,40        | deg     | Tuule suund 10 m kõrgusel  |
| WS10  | 1,56          | m/s     | Tuule kiirus 10 m kõrgusel |


* Using python script extact data from [http://airviro.klab.ee/]() (`fetch_air.ipynb`).
* Using Openrefine transform columns into correct format (use `data_tranform_steps_air.json`)
* Use Openrefine export to SQL.


* Using pandas for calculating daily and monthly mean values for each column.
* For the calculations - transformation of DateTime column into pandas datetime format and break up of date and time into separate columns.
* The results are exported as csv files daily_average.csv and monthly_average.csv



###### Metadata about electricity:

Downloaded from [http://energia.ee](), need to log in and can only be accessed by the contract owner.

| Attr  | example value | unit    | Description                 |
| ----- | ------------- | ------- | --------------------------- |
| Elec  | 2,42          |  kWh    | tunnis kulunud elekter      |
| Price | 70,03         | €/MWh   | Börsi hetke hind            |

* Downloaded file to be fixed with Openrefine (use `data_transform_steps_el.json`)
* Use Openrefine export to SQL.