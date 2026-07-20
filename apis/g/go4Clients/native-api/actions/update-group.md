# Update Group with Go4Clients

Updates an existing contact group in Go4Clients.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/groupscontacts/groups/v1.0/`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Update Group](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | ID of the group to update. |
| `groupName` | body | `string` | yes | Updated group name. |
| `filterParameters[]` | body | `array<object>` | yes | Group filter definitions. |
