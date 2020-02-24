# Smash Popularity

A data science study to measure how popular a videogame series became after one of its characters were announced to be a fighter in the Super Smash Bros. Ultimate videogame.

## Data gathering

### Popularity over time

Data was collected using [Google Trends](https://trends.google.com/trends/?geo=US), by search through each character's origin series for the last 5 years. A list of the characters can be found on the `/data/newcomers.json` file.

### Announcement dates

The dates that each character were announced was found by searching on YouTube their reveal trailers and picking the oldest one.

### Icons

A list of characters head icons (found on the `/icons` directory) was found in the [Smash Wiki](<https://www.ssbwiki.com/Category:Head_icons_(SSBU)>).

## Data processing

Python and Jupyter Notebook were used to process the data. All that was needed was to read the data collected from the Google Trends, filter the popularity from before and after the character's announcement, take the mean value and subtract them. Since they are already in percentage (relative to the search term itself), no further operation was necessary. The final dataframe was imported to a CSV file, found on `/outputs/popularity_gains.csv`.

## Data visualization

The CSV file was exported to Google Sheets. From there, a bar graph was generated and exported as a PNG image. To make it look nice, I edited it using [Pixlr](https://pixlr.com/e).

## Author

- Henrique Caúla | lhtc@cin.ufpe.br
