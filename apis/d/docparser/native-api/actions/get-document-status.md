# Get Document Status with Docparser

Retrieves status details for a Docparser document.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/document/status/:PARSER_ID/:DOCUMENT_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Get Document Status](https://docparser.com/api/#document-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes | Use the parser ID returned by List Document Parsers. |
| `DOCUMENT_ID` | path | `string` | yes | Use the document ID returned by a parsed-data action. |
