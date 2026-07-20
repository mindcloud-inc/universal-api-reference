# List Labels with Yousign

Retrieves labels from Yousign.

## Endpoint

- **Method:** `GET`
- **Path:** `/labels`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Labels](https://developers.yousign.com/reference/get-labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Pagination cursor. |
| `limit` | query | `number` | no | Maximum labels to return. |
| `name[eq]` | query | `string` | no | Return only labels whose name exactly matches this value. |
