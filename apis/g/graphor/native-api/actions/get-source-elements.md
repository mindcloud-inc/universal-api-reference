# Get Source Elements with Graphor

Retrieves parsed source elements from Graphor by file ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-elements`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Get Source Elements](https://docs.graphorlm.com/api-reference/sources/list-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | query | `string` | yes | The source file identifier whose parsed elements should be returned. |
| `page` | query | `string` | no | 1-based page number for element pagination. |
| `page_size` | query | `string` | no | Number of elements to return per page. |
