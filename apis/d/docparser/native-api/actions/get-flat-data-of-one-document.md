# Get Flat Data Of One Document with Docparser

Retrieves flat parsed data for one Docparser document.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/results/:PARSER_ID/:DOCUMENT_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Get Flat Data Of One Document](https://docparser.com/api/#get-data-of-one-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes | Use the parser ID returned by List Document Parsers. |
| `DOCUMENT_ID` | path | `string` | yes | Use the document ID returned by a parsed-data action. |
