# Get Channel Streams with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:id/streams`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Channel Streams](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token. |
| `id` | path | `string` | yes | Channel UCID. |
| `sort_by` | query | `string` | no | Streams sort order. |
