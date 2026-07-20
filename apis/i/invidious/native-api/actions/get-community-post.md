# Get Community Post with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/post/:id`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Community Post](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Community post ID. |
| `ucid` | query | `string` | no | Channel UCID for the post. |
