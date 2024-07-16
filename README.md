# Android Translation XML String Extractor

This script extracts string resources from two XML files (one in Arabic and one in English) and writes them to an Excel file. The Excel file contains three columns: the string name, the English string, and the Arabic string.

## Requirements

- Python 3.x
- `openpyxl` library

## Installation

1. Clone this repository or download the script.
2. Install the required Python package using pip:
    ```sh
    pip install openpyxl
    ```

## Usage

1. Ensure you have two XML files:
    - An Arabic strings file (e.g., `ar_strings.xml`)
    - An English strings file (e.g., `en_strings.xml`)

2. Modify the script to specify the paths to your XML files:
    ```python
    ar_strings_file = "ar_strings.xml"  
    en_strings_file = "en_strings.xml"
    output_xlsx = "extracted_strings.xlsx"
    ```

3. Run the script:
    ```sh
    python extract_strings.py
    ```

4. The script will generate an Excel file (`extracted_strings.xlsx`) containing the extracted strings.

## Functionality

The script performs the following steps:
1. Parses the Arabic and English XML files.
2. Creates a new Excel workbook and adds headers to the first sheet.
3. Iterates through the Arabic XML file, extracting the string names and their Arabic text.
4. For each Arabic string, it finds the corresponding English string in the English XML file.
5. Writes the string name, English text, and Arabic text to the Excel sheet.
6. Saves the Excel file.

## Error Handling

The script includes error handling for the following scenarios:
- Missing XML files
- Malformed XML files
- General exceptions

If an error occurs, an appropriate error message will be printed to the console.

## Example XML Files

### ar_strings.xml
```xml
<resources>
    <string name="hello">مرحبا</string>
    <string name="world">عالم</string>
</resources>
```

### en_strings.xml
```xml
<resources>
    <string name="hello">Hello</string>
    <string name="world">World</string>
</resources>
```

## License

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


