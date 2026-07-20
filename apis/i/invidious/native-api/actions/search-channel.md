# Search Channel with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:ucid/search`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Search Channel](https://docs.invidious.io/api/channels_endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Channel search page number. |
| `q` | query | `string` | yes | Search text within the channel. |
| `ucid` | path | `string` | yes | Channel UCID. |
