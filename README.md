# WeatherMan Problem - Extract Maximum Temperature

This script solves the **WeatherMan problem** by analyzing weather data stored in CSV files. It extracts the **maximum temperature** for a specified year, along with the corresponding file and date. The data files are expected to be organized in a directory, and the script processes them based on the specified year and target column.

---

## Features

- **Year-Based File Matching**: Automatically processes files containing the specified year in their names.
- **Column Extraction**: Extracts data from a specified column, such as `Max TemperatureC`.
- **Max Temperature Identification**: Identifies and displays the highest temperature, its associated date, and the file containing it.
- **Error Handling**: Skips invalid or empty data entries.

---

## Requirements

To use this script, ensure the following:

1. **Python 3.x**: Installed on your system.
2. **CSV Weather Data Files**: Organized in the specified folder structure.
3. **Target Column Availability**: The target column (e.g., `Max TemperatureC`) must exist in the CSV files.

---

## Installation

1. Clone the repository or download the script file:
   ```bash
   git clone https://github.com/your-repo/weatherman-problem.git
   ```
2. Navigate to the directory:
   ```bash
   cd weatherman-problem
   ```

---

## Folder Structure

Ensure your weather data is organized as follows:

```
dataset/
└── Dubai_weather/
    ├── Dubai_weather_2004.csv
    ├── Dubai_weather_2005.csv
    ├── ...
```

### Example CSV File Format
Each CSV file should have a structure like this:
```
Date,Max TemperatureC,Min TemperatureC
2004-01-01,32,21
2004-01-02,35,23
```

---

## How to Use

### 1. Update Script Parameters
Open the script and adjust the following variables as needed:

- **`folder_name`**: Name of the folder containing weather data (default: `Dubai_weather`).
- **`year`**: Year to filter relevant files (default: `2004`).
- **`column_to_extract`**: Column name to extract data from (default: `Max TemperatureC`).

### 2. Run the Script
Execute the script from the terminal:
```bash
python extract_max_temperature.py
```

### 3. View the Output
The script will print:
- The **maximum temperature** found.
- The **date** associated with the maximum temperature.
- The **file name** containing the maximum temperature.

---

## Example Output

Given a dataset with the file `Dubai_weather_2004.csv`, the output might look like this:

```plaintext
Processing file: Dubai_weather_2004.csv
Maximum Temperature: 45.5
Date (from first column): 2004-06-15
File: Dubai_weather_2004.csv
```

---

## Notes

1. **CSV File Validation**:
   - Ensure all CSV files include the column specified in `column_to_extract`.
2. **Empty Values**:
   - Rows with empty or invalid data in the target column are skipped.
3. **File Filtering**:
   - Only `.csv` files are processed, and filenames must contain the specified year.

---

## Troubleshooting

- **File or Directory Not Found**:
  - Verify the `dataset/Dubai_weather/` folder exists and contains relevant `.csv` files.
- **Incorrect Column Name**:
  - Ensure the `column_to_extract` value matches the column name in your CSV files exactly.

---

## License

This script is licensed under the [MIT License](LICENSE).

---
