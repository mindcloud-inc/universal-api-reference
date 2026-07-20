# Update Item with MRPeasy

Updates an existing stock item in MRPeasy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/{{articleId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Update Item](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | path | `number` | yes | MRPeasy article ID. |
| `code` | body | `string` | no | Updated item code. |
| `title` | body | `string` | no | Updated item title. |
