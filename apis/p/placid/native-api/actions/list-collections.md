# List Collections with Placid

Retrieves collections from Placid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/rest/collections`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [List Collections](https://placid.app/docs/2.0/rest/collections#index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Number of collections to return per page (max 100). |
| `cursor` | query | `string` | no | Cursor for the next page of collections. |
