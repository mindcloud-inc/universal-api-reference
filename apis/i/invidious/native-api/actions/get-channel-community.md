# Get Channel Community with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:id/community`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Channel Community](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `continuation` | query | `string` | no | Continuation token. |
| `id` | path | `string` | yes | Channel UCID. |
