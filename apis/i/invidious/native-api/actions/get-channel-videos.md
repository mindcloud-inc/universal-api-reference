# Get Channel Videos with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:id/videos`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Channel Videos](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token. |
| `id` | path | `string` | yes | Channel UCID. |
| `sort_by` | query | `string` | no | Videos sort order. |
