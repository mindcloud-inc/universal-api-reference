# CSV to Text with Weavo Liquid Loom

Creates text output from CSV in Weavo Liquid Loom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/CsvToText`
- **Base URL:** `https://liquidloom.weavo.no`
- **Official documentation:** [CSV to Text](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#csv-to-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputString` | body | `string` | yes | Input string in CSV format. |
| `liquidTemplate` | body | `string` | no | Optional Liquid template code generated at weavo.dev. For CSV inputs, iterate over the parsed data array for custom mappings. |
| `logFileName` | body | `string` | no | Name of the log file. Only applicable when logging is enabled. |
