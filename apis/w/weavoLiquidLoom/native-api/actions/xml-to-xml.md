# XML to XML with Weavo Liquid Loom

Creates XML output from XML in Weavo Liquid Loom.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/XmlToXml`
- **Base URL:** `https://liquidloom.weavo.no`
- **Official documentation:** [XML to XML](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#xml-to-xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputString` | body | `string` | yes | Input string in XML format. |
| `liquidTemplate` | body | `string` | no | Optional Liquid template code generated at weavo.dev for custom mappings. XML values are addressed from their root element path. |
| `logFileName` | body | `string` | no | Name of the log file. Only applicable when logging is enabled. |
