# Get Data Of Multiple Documents By Remote ID with Docparser

Retrieves parsed data for Docparser documents by remote ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/results/:PARSER_ID`
- **Base URL:** `https://api.docparser.com`
- **Official documentation:** [Get Data Of Multiple Documents By Remote ID](https://docparser.com/api/#get-data-of-multiple-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PARSER_ID` | path | `string` | yes | Use the parser ID returned by List Document Parsers. |
| `remote_id` | query | `string` | yes | Return only parsed documents that match this remote ID. |
| `include_processing_queue` | query | `boolean` | no | Include documents that are still waiting in the processing queue. |
