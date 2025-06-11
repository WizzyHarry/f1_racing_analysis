## Pre-Processing

<b>At the time of this data analysis, I was unaware of the various pre-processing stratigies I could've
utilized to streamline my work. All pre-processing steps were down directly in RStudio.
They can be found in my poorly named R file which DOES encompass all aspects of the analysis.</b>

#### Pre-Processing Steps

<p>The Ergast API is a specific F1 API that encompasses all F1 racing data from 1969-2024.
Creating a relational database, the Relationship Diagram can be seen below. The only outsourced
data came from Racingpass, an independent blog that tallied overtakes for all drivers every race.</p>

<p> Pre-processing steps included</p>
<ul>
  <li>Connecting driver to driver_id</li>
  <li>Connecting race to race_id</li>
  <li>Creating qualifying quarters</li>
  <li>Adjusting null values</li>
  <li>Adjusting data types</li>
</ul>

<p></n>Racingpass had their overtakes neatly arranged in a .csv file, with fields such as overtaker,
overtaken, place taking. I replaced overtaker/taken fields with driver_Id's, and used the place
taking column to calculate the "importance of an overtake", more can be found in the Point Values section.</p>

### Sources

<b>All compiled statistical data came from Ergast F1 API & Racing Pass</b>

[Ergast API](https://ergast.com/mrd/)

[Racing Pass](https://racingpass.net/)

#### Files

<b>R file</b>

[F1_data_analysis_R](avg_lap_times.R)

<b> CSV's & Zip </b>

[circuits.csv](circuits.csv)

[drivers.csv](drivers.csv)

[lap_times.csv](lap_times.csv)

[overtakes.csv](overtakes.csv)

[pit_stops.csv](pit_stops.csv)

[qualifying.csv](qualifying.csv)

[races.csv](races.csv)

[results.csv](results.csv)

[f1db_csv.zip](f1db_csv.zip)

[driver_names](driver_names.txt)

<b>API DB Relationship Diagram</b>

![Ergast_DB](ergast_db-1.png)