# SAP CPI – Order Processing Integration

## Project Overview
This project processes multiple customer orders using SAP Cloud Integration (CPI). It validates order details, routes valid orders based on their type, converts XML data to CSV, and stores the results in separate Data Stores.

## Business Requirements
- Process multiple customer orders independently.
- Validate Order ID, Customer ID, and Quantity.
- Separate valid and invalid orders.
- Route valid orders into Domestic and International branches.
- Convert valid XML orders into CSV format.
- Store processed orders in separate Data Stores.

## SAP CPI Components Used
- Timer Start Event
- Content Modifier
- JSON to XML Converter
- General Splitter
- Groovy Script
- Router
- XML to CSV Converter
- Data Store Write

## Integration Flow
Timer → Content Modifier → JSON to XML → General Splitter → Groovy Validation → Validation Router → Order Type Router → XML to CSV → Data Store Write

## Testing Results
| Order ID | Validation | Result |
|---|---|---|
| ORD101 | Invalid | Rejected |
| ORD102 | Valid | International Data Store |
| ORD103 | Valid | Domestic Data Store |
| ORD104 | Valid | International Data Store |

## Project Files
- **iFlow ZIP:** SAP CPI integration flow
- **Documentation PDF:** Detailed configuration and screenshots
- **sample_orders.json:** Sample input payload

## Conclusion
Successfully implemented and tested an SAP CPI Order Processing Integration with validation, routing, data conversion, and Data Store persistence.
