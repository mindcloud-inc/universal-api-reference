# Extract Structured Data with Graphor

Extracts structured data from Graphor documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/run-extraction`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Extract Structured Data](https://docs.graphorlm.com/api-reference/extract-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids` | body | `string` | yes | Preferred list of file IDs to extract from. |
| `output_schema` | body | `string` | yes | JSON Schema describing the extraction result structure. |
| `thinking_level` | body | `string` | no | Optional thinking level: fast, balanced, or accurate. |
| `user_instruction` | body | `string` | yes | Natural-language instructions that guide the extraction. |
