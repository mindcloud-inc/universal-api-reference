# Get Channel Podcasts with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:id/podcasts`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Channel Podcasts](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token. |
| `id` | path | `string` | yes | Channel UCID. |
