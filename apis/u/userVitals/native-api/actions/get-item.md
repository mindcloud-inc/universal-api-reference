# Get Item with UserVitals

Retrieves an item by token from the roadmap API.

## Endpoint

- **Method:** `GET`
- **Path:** `/items/:publicItemTokenId`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Get Item](https://api.roadmap.space/#get-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicItemTokenId` | path | `string` | yes | The Base64-encoded public item token id. |
