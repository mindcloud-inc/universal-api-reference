# List Parser Model Layouts with Docparser

Retrieves parser model layouts from Docparser.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/parser/models/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [List Parser Model Layouts](https://docparser.com/api/#list-parser-model-layouts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes | Use the parser ID returned by List Document Parsers. |
