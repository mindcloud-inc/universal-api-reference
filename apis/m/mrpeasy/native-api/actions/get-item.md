# Get Item with MRPeasy

Retrieves a stock item from MRPeasy.

## Endpoint

- **Method:** `GET`
- **Path:** `/items/{{articleId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Get Item](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | path | `number` | yes | MRPeasy article ID. |
