# XML to Text with Weavo Liquid Loom

Creates text output from XML in Weavo Liquid Loom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/XmlToText`
- **Base URL:** `https://liquidloom.weavo.no`
- **Official documentation:** [XML to Text](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#xml-to-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputString` | body | `string` | yes | Input string in XML format. |
| `liquidTemplate` | body | `string` | no | Optional Liquid template code generated at weavo.dev for custom mappings. XML values are addressed from their root element path. |
| `logFileName` | body | `string` | no | Name of the log file. Only applicable when logging is enabled. |
