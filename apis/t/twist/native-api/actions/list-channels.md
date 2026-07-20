# List Channels with Twist

Retrieves channels from a Twist workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/get`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [List Channels](https://developer.twist.com/v3/#get-all-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | If enabled, only archived conversations are returned. |
| `workspace_id` | query | `number` | yes | The id of the workspace. |
