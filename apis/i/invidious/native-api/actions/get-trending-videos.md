# Get Trending Videos with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/trending`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Trending Videos](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | query | `string` | no | ISO 3166 country code. |
| `type` | query | `string` | no | Trending type: music, gaming, movies, or default. |
