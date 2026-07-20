# Replace Group with UseINBOX

Replaces an existing group in UseINBOX.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inbox/v1/groups/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Replace Group](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Group ID from INBOX. |
| `groupName` | body | `string` | yes | Group name. |
