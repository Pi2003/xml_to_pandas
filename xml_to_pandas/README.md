# XML to DataFrame Converter

## Overview

This Python utility provides a robust and flexible solution for converting XML files into pandas DataFrames. The library offers advanced parsing capabilities that can handle complex XML structures, including nested elements, attributes, and varying node types.

## Features

- 🔄 Recursive XML parsing
- 🌳 Handles nested and complex XML structures
- 🏷️ Optional namespace removal
- 📊 Converts XML to pandas DataFrame
- 🔧 Configurable root tag preservation
- 🚨 Comprehensive error handling and logging

## Requirements

- Python 3.7+
- pandas
- xml.etree.ElementTree (Standard Library)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Pi2003/xml_to_pandas.git
cd xml_to_pandas
```

2. Install dependencies:
```bash
pip install pandas
pip install xml_to_pandas
```

## Usage

### Basic Example

```python
from xml_to_pandas import xml_to_pandas

# Convert XML to DataFrame
df = xml_to_pandas.convert('your_file.xml')
print(df)
```

### Advanced Usage

```python
# Ignore XML namespaces
df = xml_to_pandas.convert('your_file.xml', ignore_namespaces=True)

# Control root tag preservation
df = xml_to_pandas.convert('your_file.xml', preserve_root_tag=False)
```

## Parsing Behavior

The converter handles different XML structures intelligently:

- 📍 **Leaf Nodes**: Converted to single-row DataFrames
- 🌿 **Parent Nodes with Leaf Children**: Concatenated side by side
- 🌳 **Parent Nodes with Parent Children**: Concatenated vertically
- 🔀 **Mixed Node Types**: Intelligently merged

## Logging

The library uses Python's standard logging module to provide informative runtime messages:
- File not found errors
- XML parsing errors
- Unexpected exceptions

## Error Handling

- Returns `None` for parsing failures
- Logs detailed error messages
- Handles various XML parsing scenarios

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Pinak Tendulkar - pdtendulkar140203@gmail.com

Project Link: [https://github.com/Pi2003/xml_to_pandas](https://github.com/Pi2003/xml_to_pandas)
