# Update Group with Hex

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/{groupId}`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Update Group](https://learn.hex.tech/docs/api-integrations/api/reference#operation/EditGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Unique ID for a group. |
| `members.add.users[].id` | body | `string<string>` | no | — |
| `members.remove.users[].id` | body | `string<string>` | no | — |
| `name` | body | `string` | no | — |
