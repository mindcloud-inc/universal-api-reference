# Delete Links with Raven Tools

Deletes existing links from Raven Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://api.raventools.com`
- **Official documentation:** [Delete Links](https://api.raventools.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Optional domain if omitted from each link record. |
| `link` | query | `string` | yes | JSON-encoded string representing one or more Raven link ids to delete. |
