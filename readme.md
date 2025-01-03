# Worldwide Ports Dataset

This repository contains a JSON dataset of 3,898 worldwide ports, including their latitude and longitude. The list was generated using **Pub 150**, various networking tools, and OpenAI's API. 

![World Map of Ports](static/map.png)

## Dataset Structure

The dataset provides the following details for each port:

- **CITY**: The city where the port is located.
- **STATE**: The state or region.
- **COUNTRY**: The country where the port is situated.
- **LATITUDE**: The latitude of the port.
- **LONGITUDE**: The longitude of the port.

### Example JSON Entries
```json
[
    {"CITY":"Aabenraa","STATE":"South Denmark","COUNTRY":"Denmark","LATITUDE":55.04,"LONGITUDE":9.42},
    {"CITY":"Laâyoune","STATE":"Western Sahara","COUNTRY":"Morocco","LATITUDE":27.07,"LONGITUDE":-13.47},
    {"CITY":"Aalborg","STATE":"North Jutland","COUNTRY":"Denmark","LATITUDE":57.05,"LONGITUDE":9.92}
]
```

## Example Usage: Finding a Port by City Name

The following Python example demonstrates how to search for a port by city name:

```python
import json

# Function to find a port by city name
def find_port_by_city(file_path, city_name):
    try:
        # Load the JSON data
        with open(file_path, 'r', encoding='utf-8') as file:
            data = json.load(file)

        # Find the port by city name
        for port in data:
            if port.get("CITY") == city_name:
                return port

        return None  # Return None if no match is found
    except Exception as e:
        print(f"An error occurred: {e}")

# Example usage
city_to_find = "Aalborg"
file_path = "/path/to/ports.json"  # Replace with the actual path to your JSON file
result = find_port_by_city(file_path, city_to_find)

if result:
    print(f"Port found: {result}")
else:
    print(f"No port found for city: {city_to_find}")
```

### Output Example
For the city `"Aalborg"`, the script outputs:
```plaintext
Port found: {'CITY': 'Aalborg', 'STATE': 'North Jutland', 'COUNTRY': 'Denmark', 'LATITUDE': 57.05, 'LONGITUDE': 9.92}
```

## Use Cases

This dataset can be utilized in various domains, for example:

- **Grounded Truth**: For model creation.
- **Prompt fine-tuning**: For fine-tuning models.
- **Routing**: Developing maritime and logistic routes.
- **ETA Predictions**: For use with time of arrival calculations.

## Contribution

We welcome contributions and suggestions to improve the dataset. Feel free to:

- Submit issues or enhancements via the [GitHub Issues page](#).
- Fork the repository and submit pull requests with updates or new data.

## Additional Resources

For a detailed explanation of how this dataset was created and potential use cases, check out our [Medium article](https://placeholder-link.com).

## Contact

If you have any questions or would like to contribute, please reach out via [LinkedIn](https://www.linkedin.com/in/tayljordan/).