# Get Source Elements By Type with Graphor

Retrieves parsed source elements from Graphor by element type.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-elements`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Get Source Elements By Type](https://docs.graphorlm.com/api-reference/sources/list-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | query | `string` | yes | The source file identifier whose parsed elements should be returned. |
| `page` | query | `string` | no | 1-based page number for element pagination. |
| `page_size` | query | `string` | no | Number of elements to return per page. |
| `type` | query | `string` | yes | Optional element type filter such as NarrativeText, Title, or Table. |
