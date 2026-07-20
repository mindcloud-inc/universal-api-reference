# List User Actions with Discourse

Retrieves recent user actions from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/user_actions.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List User Actions](https://docs.discourse.org/#tag/Users/operation/listUserActions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | User action filter value documented by Discourse. |
| `offset` | query | `string` | yes | Zero-based offset into the user actions feed. |
| `username` | query | `string` | yes | Discourse username whose actions should be listed. |
