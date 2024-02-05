# Divemeets Data Scraper
Retrive and calculate competition performances from [www.divemeets.com](https://secure.meetcontrol.com/divemeets/system/index.php) for an individual diver. 

## Installation
Install the required packages:
    `pip install -r requirements.txt`

Valid diver names can be found on the [divemeets website](https://secure.meetcontrol.com/divemeets/system/memberlist.php)

## Usage: 

### Get Event Data: `python EventData.py "Conrad Eck"`
* Creates a csv containing event performance history for the given diver at `diver_csvs/<diver_name>.csv`
* Calculates the `Z-Score`, `Mean`, and `Standard Deviation` of the divers score compared to others for each event

| Diver     | Date       | Board                | Place | Competitors Count | Final Score | Z-Score | Mean  | Standard Deviation |
|-----------|------------|----------------------|-------|-------------------|-------------|---------|-------|-------------------|
| Conrad Eck| 02-03-2024 | Men Platform (6 Dives)| 6    | 8                 | 299.25      | -0.36   | 317.24| 49.82             |

*Example row from Conrad_Eck.csv*

### Merge CSV Data: `python merge_csv_data.py`
* Merges csv data for each diver within `diver_csvs/` for comparative analysis
* Produces `merged_data/divers_combined.csv`

