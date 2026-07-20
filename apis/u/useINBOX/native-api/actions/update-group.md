# Update Group with UseINBOX

Updates an existing group in UseINBOX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inbox/v1/groups/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Update Group](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Group ID from INBOX. |
| `groupName` | body | `string` | no | Updated group name. |
