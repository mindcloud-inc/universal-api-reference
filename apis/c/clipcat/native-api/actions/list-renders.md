# List Renders with Clipcat

Retrieves video renders for the current Clipcat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/renders`
- **Base URL:** `https://api.clipcat.com`
- **Official documentation:** [List Renders](https://developers.clipcat.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `completed` | query | `boolean` | no | Set to true to return only completed renders. |
| `page` | query | `number` | no | The page number of render results to retrieve. |
| `template` | query | `string` | no | Filter renders by template UID. |
