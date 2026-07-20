# Delete Source with Graphor

Deletes an existing source from Graphor by file ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/delete`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Delete Source](https://docs.graphorlm.com/api-reference/sources/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | The unique identifier of the source to delete. |
