# Get Sorted Data Of Multiple Documents with Docparser

Retrieves sorted parsed data for multiple Docparser documents.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/results/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Get Sorted Data Of Multiple Documents](https://docparser.com/api/#get-data-of-multiple-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes | Use the parser ID returned by List Document Parsers. |
| `sort_by` | query | `string` | yes | Choose the field Docparser should sort by. |
| `sort_order` | query | `string` | no | Choose whether Docparser sorts ascending or descending. Accepted values: `0`, `1`. |
| `limit` | query | `number` | no | Maximum number of parsed documents to return. |
| `include_processing_queue` | query | `boolean` | no | Include documents that are still waiting in the processing queue. |
