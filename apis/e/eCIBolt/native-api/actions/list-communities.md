# List Communities with ECI Bolt

## Endpoint

- **Method:** `GET`
- **Path:** `/open/v1/communities`
- **Base URL:** `https://app.bolttech.net`
- **Official documentation:** [List Communities](https://app.bolttech.net/api-docs/index.html#/Communities/get_open_v1_communities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | no | Token used to get the changed communities, returned on the last page of the communities. You should only send the refresh_token or the next_batch. |
| `refresh` | query | `string` | no | Return only directly changed records when value is "self" |
