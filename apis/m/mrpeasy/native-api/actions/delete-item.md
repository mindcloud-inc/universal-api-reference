# Delete Item with MRPeasy

Deletes an existing stock item from MRPeasy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/items/{{articleId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Delete Item](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | path | `number` | yes | MRPeasy article ID. |
