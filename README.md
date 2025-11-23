# bmrcl-ridership-hourly

Dataset of hourly station-wise ridership on the Namma Metro subway network operated by BMRCL in Bengaluru, India. Sourced from RTI.

Explore the dataset:
- [Station hourly ridership](https://hyparam.github.io/demos/hyparquet/?key=https%3A%2F%2Fraw.githubusercontent.com%2FVonter%2Fbmrcl-ridership-hourly%2Fmain%2Fdata%2Fstation-hourly.parquet).
- [Station hourly ridership (exits)](https://hyparam.github.io/demos/hyparquet/?key=https%3A%2F%2Fraw.githubusercontent.com%2FVonter%2Fbmrcl-ridership-hourly%2Fmain%2Fdata%2Fstation-hourly-exits.parquet).
- [Station pair hourly ridership](https://hyparam.github.io/demos/hyparquet/?key=https%3A%2F%2Fraw.githubusercontent.com%2FVonter%2Fbmrcl-ridership-hourly%2Fmain%2Fdata%2Fstationpair-hourly.parquet).

## Data

* [station-hourly.parquet](data/station-hourly.parquet?raw=1): Station hourly ridership as Parquet file.
* [station-hourly.csv.zip](data/station-hourly.csv.zip?raw=1): Station hourly ridership as CSV compressed in a Zip file.
* [station-hourly-exits.parquet](data/station-hourly-exits.parquet?raw=1): Station hourly ridership (exits) as Parquet file.
* [station-hourly-exits.csv.zip](data/station-hourly-exits.csv.zip?raw=1): Station hourly ridership (exits) as CSV compressed in a Zip file.
* [stationpair-hourly.parquet](data/stationpair-hourly.parquet?raw=1): Station pair hourly ridership as Parquet file.
* [stationpair-hourly.csv.zip](data/stationpair-hourly.csv.zip?raw=1): Station pair hourly ridership as CSV compressed in a Zip file.
* [stationpair-hourly-enhanced.parquet](data/stationpair-hourly-enhanced.parquet?raw=1): Station pair hourly ridership with enriched fields as Parquet file.
* [stationpair-hourly-enhanced.csv.zip](data/stationpair-hourly-enhanced.csv.zip?raw=1): Station pair hourly ridership with enriched fields as CSV compressed in a Zip file.

For more details, refer to the [DATA.md](DATA.md).

## Visualizations

- [How Bangalore Uses The Metro](https://diagramchasing.fun/2025/how-bangalore-uses-the-metro)

## Scripts

- [parse.py](parse.py): Parses the raw Excel files to generate the Parquet and CSV datasets

## License

This bmrcl-ridership-hourly dataset is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/. 
Some individual contents of the database are under copyright by BMRCL.

You are free:

* **To share**: To copy, distribute and use the database.
* **To create**: To produce works from the database.
* **To adapt**: To modify, transform and build upon the database.

As long as you:

* **Attribute**: You must attribute any public use of the database, or works produced from the database, in the manner specified in the ODbL. For any use or redistribution of the database, or works produced from it, you must make clear to others the license of the database and keep intact any notices on the original database.
* **Share-Alike**: If you publicly use any adapted version of this database, or works produced from an adapted database, you must also offer that adapted database under the ODbL.
* **Keep open**: If you redistribute the database, or an adapted version of it, then you may use technological measures that restrict the work (such as DRM) as long as you also redistribute a version without such measures.

## Generating

Ensure that `python` and the required dependencies in `requirements.txt` are installed.

```
# Parse the Excel files
python parse.py
```

## Credits

- [BMRCL](https://english.bmrc.co.in/)

## AI Declaration

Components of this repository, including code and documentation, were written with assistance from Claude AI.
