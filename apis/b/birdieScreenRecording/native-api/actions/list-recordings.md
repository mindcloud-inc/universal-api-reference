# List Recordings with Birdie Screen Recording

Retrieves recordings from Birdie Screen Recording.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/videos`
- **Base URL:** `https://app.birdie.so`
- **Official documentation:** [List Recordings](https://docs.birdie.so/birdie-docs/birdie-api/reference/api-reference/list-recordings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket` | query | `string` | no | Filter recordings by ticket id. |
| `email` | query | `string` | no | Filter recordings by customer email. |
| `param` | query | `string` | no | Filter recordings by a metadata key added to the recording link. |
| `value` | query | `string` | no | Metadata value to match for the selected metadata key. |
