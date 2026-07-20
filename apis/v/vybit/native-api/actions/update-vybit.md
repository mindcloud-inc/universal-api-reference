# Update Vybit with Vybit

## Endpoint

- **Method:** `PATCH`
- **Path:** `/vybit/{{key}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Update Vybit](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access` | body | `string` | no | Vybit visibility and access control |
| `description` | body | `string` | no | Detailed vybit description |
| `imageUrl` | body | `string` | no | Default image URL for notifications |
| `key` | path | `string` | yes | The unique key of the vybit. |
| `linkUrl` | body | `string` | no | Default link URL for notifications |
| `message` | body | `string` | no | Default notification message |
| `name` | body | `string` | no | Vybit display name |
| `sendPermissions` | body | `string` | no | Who can trigger and receive notifications |
| `soundKey` | body | `string` | no | Sound key from the Sounds endpoint |
| `status` | body | `string` | no | Vybit status |
| `triggerType` | body | `string` | no | How the vybit is triggered |
