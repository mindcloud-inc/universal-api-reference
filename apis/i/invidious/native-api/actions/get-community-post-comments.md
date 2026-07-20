# Get Community Post Comments with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/post/:id/comments`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Community Post Comments](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Community post ID. |
| `sort_by` | query | `string` | no | Comment sort order. |
| `ucid` | query | `string` | yes | Channel UCID for the post comments. |
