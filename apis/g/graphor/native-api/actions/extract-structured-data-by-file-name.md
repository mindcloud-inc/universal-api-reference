# Extract Structured Data By File Name with Graphor

Extracts structured data from Graphor documents by file name.

## Endpoint

- **Method:** `POST`
- **Path:** `/run-extraction`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Extract Structured Data By File Name](https://docs.graphorlm.com/api-reference/extract-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_names` | body | `string` | yes | Deprecated list of file names to extract from when file IDs are not available. |
| `output_schema` | body | `string` | yes | JSON Schema describing the extraction result structure. |
| `user_instruction` | body | `string` | yes | Natural-language instructions that guide the extraction. |
