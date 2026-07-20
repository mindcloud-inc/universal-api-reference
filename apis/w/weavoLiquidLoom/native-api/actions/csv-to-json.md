# CSV to JSON with Weavo Liquid Loom

Creates JSON output from CSV in Weavo Liquid Loom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/CsvToJson`
- **Base URL:** `https://liquidloom.weavo.no`
- **Official documentation:** [CSV to JSON](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#csv-to-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputString` | body | `string` | yes | Input string in CSV format. |
| `liquidTemplate` | body | `string` | no | Optional Liquid template code generated at weavo.dev. For CSV inputs, iterate over the parsed data array for custom mappings. |
| `logFileName` | body | `string` | no | Name of the log file. Only applicable when logging is enabled. |
