# bmrcl-ridership-hourly

The data was sourced from an RTI. The responses from the RTI are in the form of Excel files:
- [august/station-hourly.xlsx](raw/august/station-hourly.xlsx): Station hourly ridership for August 2025
- [august/stationpair-hourly.xlsx](raw/august/stationpair-hourly.xlsx): Station pair hourly ridership for August 2025
- [september/station-hourly.xlsx](raw/september/station-hourly.xlsx): Station hourly ridership for September 2025

Data covers the following periods:
- Station Hourly Ridership:
  - 1st August 2025 to 18th August 2025
  - 1st September 2025 to 30th September 2025
- Station Pair Hourly Ridership:
  - 1st August 2025 to 18th August 2025

## Data dictionary

### Station hourly ridership

| Variable | Type | Description |
|----------|------|-------------|
| Date | string | Date when the ridership was recorded (format: YYYY-MM-DD) |
| Hour | int64 | Hour of the day when the ridership was recorded (0-23) |
| Station | string | Station name (83 unique stations) |
| Ridership | int64 | Ridership count (Number of passengers boarded at the station during the hour) |

### Station hourly ridership (exits)

| Variable | Type | Description |
|----------|------|-------------|
| Date | string | Date when the ridership was recorded (format: YYYY-MM-DD) |
| Hour | int64 | Hour of the day when the ridership was recorded (0-23) |
| Station | string | Station name (83 unique stations) |
| Ridership | int64 | Ridership count (Number of passengers deboarded at the station during the hour) |

### Station pair hourly ridership

| Variable | Type | Description |
|----------|------|-------------|
| Date | string | Date when the ridership was recorded (format: YYYY-MM-DD) |
| Hour | int64 | Hour of the day when the ridership was recorded (0-23) |
| Origin Station | string | Origin station name (83 unique stations) |
| Destination Station | string | Destination station name (83 unique stations) |
| Ridership | int64 | Ridership count (Number of passengers boarded at the origin station and alighted at the destination station during the hour) |


### Station pair hourly ridership (enhanced)

| Variable | Type | Description |
|----------|------|-------------|
| Date | string | Date when the ridership was recorded (format: YYYY-MM-DD) |
| Hour | int64 | Hour of the day when the ridership was recorded (0-23) |
| Origin Station | string | Origin station name (83 unique stations) |
| Destination Station | string | Destination station name (83 unique stations) |
| Ridership | int64 | Ridership count (Number of passengers boarded at the origin station and alighted at the destination station during the hour) |
| Travelled Stations | int64 | No. of stations travelled for this station pair, excluding origin station |
| Fare Slab | int64 | Fare Slab for this station pair used for calculating the fare |
| Fare | int64 | Fare for this station pair excluding discounts |
| Revenue | int64 | Total revenue from this ridership for this station pair |


### Station Names

The original Excel file for station hourly ridership uses old station names instead of current station names. The old station names are mapped to current station names using the [station-names.csv](raw/station-names.csv) file.

The original Excel file for station pair hourly ridership uses station codes instead of station names. The station codes are mapped to station names using the [station-codes.csv](raw/station-codes.csv) file.

## Data source

The data was sourced from an RTI, filed with the help of documentation on filing an RTI by [Zen Citizen](https://zencitizen.in/2024/12/29/what-to-expect-when-you-are-filing-an-rti-application/).

The body of the August 2025 RTI request was as follows:

```
I request the following information under Section 6(1) of the RTI Act, 2005.

Period to which the information relates: August 2025

1. Please provide the details of hour-wise passenger entry and exit numbers at each metro station in Namma Metro for each day during the period: From 1th August 2025 to 18th August 2025

2. Please provide the individual raw data for each metro station separately, not summarized data for all stations combined. Please provide each hour data separately, not summarized data for the entire day combined.

3. Please provide the information in an Excel or CSV format for easy analysis to the email address mentioned.

4. As per Section 4 of the RTI Act, 2005, if the above information is in the public domain, kindly provide the Links/URLs of the said websites.
  - https://english.bmrc.co.in/ridership/ does not provide data for hour-wise passenger entry and exit numbers at individual stations.

5. As per Section 6 (3) of the RTI Act, where an application is made to a public authority requesting for an information which is held by another public authority, or the subject matter of which is more closely connected with the functions of another public authority, the public authority to which such application is made shall transfer the application or such part of it as may be appropriate to that other public authority and inform the applicant immediately about such transfer.

6. As per section 7(3) of the RTI Act 2005, In case, there are further fee required to provide the requested information, I request the PIO to inform me of the additional fee amount along with the calculations made to arrive at the amount.

7. As per section 7(8)(iii) and 7(3)(ii) of the RTI Act 2005, I request the PIO to inform me of the particulars of First Appellate Authority.

8. Kindly provide the information within the stipulated time of 30 days.
```
