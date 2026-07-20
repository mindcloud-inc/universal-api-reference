# Delete Tag with UniOne

Deletes an existing tag from UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `tag/delete.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Delete Tag](https://docs.unione.io/en/web-api-ref#tag-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | body | `number` | yes | Unique tag identifier returned by List Tags. |
