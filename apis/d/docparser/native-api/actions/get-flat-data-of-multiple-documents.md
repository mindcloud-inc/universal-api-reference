# Get Flat Data Of Multiple Documents with Docparser

Retrieves flat parsed data for multiple Docparser documents.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/results/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Get Flat Data Of Multiple Documents](https://docparser.com/api/#get-data-of-multiple-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes | Use the parser ID returned by List Document Parsers. |
| `list` | query | `string` | no | Choose which parsed documents to return. Accepted values: `0`, `1`, `2`. |
| `limit` | query | `number` | no | Maximum number of parsed documents to return. |
| `date` | query | `number` | no | Provide a UNIX timestamp when the selected list mode requires a date boundary. |
| `include_processing_queue` | query | `boolean` | no | Include documents that are still waiting in the processing queue. |
