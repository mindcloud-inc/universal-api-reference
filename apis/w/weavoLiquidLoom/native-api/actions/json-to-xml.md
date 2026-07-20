# JSON to XML with Weavo Liquid Loom

Creates XML output from JSON in Weavo Liquid Loom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/JsonToXml`
- **Base URL:** `https://liquidloom.weavo.no`
- **Official documentation:** [JSON to XML](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#json-to-xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputString` | body | `string` | yes | Input string in JSON format. |
| `liquidTemplate` | body | `string` | no | Optional Liquid template code generated at weavo.dev for custom mappings. |
| `logFileName` | body | `string` | no | Name of the log file. Only applicable when logging is enabled. |
