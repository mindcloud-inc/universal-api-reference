# Update Group with Blooio Messaging

Updates an existing group in Blooio Messaging.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/{groupId}`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Update Group](https://docs.blooio.com/groups/updateGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Group identifier. |
| `name` | body | `string` | no | Group name. |
