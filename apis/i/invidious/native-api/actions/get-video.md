# Get Video with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:id`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Video](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | YouTube/Invidious video ID. |
| `region` | query | `string` | no | ISO 3166 country code. |
