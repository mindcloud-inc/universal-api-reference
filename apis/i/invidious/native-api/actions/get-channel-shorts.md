# Get Channel Shorts with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:id/shorts`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Channel Shorts](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token. |
| `id` | path | `string` | yes | Channel UCID. |
| `sort_by` | query | `string` | no | Shorts sort order. |
